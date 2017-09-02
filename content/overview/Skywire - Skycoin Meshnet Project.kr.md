+++
title = "스카이와이어 - 스카이코인 메쉬넷(Meshnet) 프로젝트"
tags = [
    "Skywire",
    "Meshnet",
]
date = "2017-08-29"
categories = [
    "Skywire",
    "Overview",
]
+++

![Skywire: The New Internet](https://i.imgur.com/9Jk0gLe.jpg)

<!-- MarkdownTOC autolink="true" bracket="round" -->

- [소개](#introduction)
- [라우팅 : 개요](#routing-overview)
- [보상 : 보상 프로토콜](#incentives-payment-protocol)
- [소스 라우팅 : 링크 계층 암호화](#source-routing-link-layer-encryption)
    - [프로토콜 예시 : Nodes `A` and `B`](#example-protocol-nodes-a-and-b)
    - [가능성 있는 개선사항:](#possible-improvements)
- [IPv4 게이트웨이 : 현재의 IPS를 경유하는](#ipv4-gateway-bypassing-existing-isps)
    - [예제 1](#example-one)
    - [예제 2](#example-two)
- [스카이와이어 데몬 서비스 아키텍쳐](#skywire-daemon-services-architecture)
    - [서비스 예제 : 블럭체인 동기화](#example-service-blockchain-sync)
- [멀티-홈 라우팅 및 링크 집계](#multi-home-routing-and-link-aggregation)
- [메쉬넷 라우팅 : 저장 및 전송](#meshnet-routing-store-and-forward)
- [저장 및 전송 : 용량 활용](#store-and-forward-capacity-utilization)
- [저장 및 전송 : 예제](#store-and-forward-examples)
    - [정상 작동의 예](#example-of-normal-operation)
    - [혼잡이 있는 경우의 예](#example-with-congestion)
    - [패킷 손실이 있는 경우의 예](#example-with-packet-loss)
- [소스라우팅 : 대역폭 시간지연 작업](#store-and-forward-bandwidth-latency-product)
- [저장 및 전송 : 용량 활용도, 서비스 품질](#store-and-forward-capacity-utilization-quality-and-service)
- [소스 라우팅 : 다중 경로 모바일 연결](#source-routing-multi-route-mobile-connectivity)
- [소스 라우팅 : 노드 보안](#source-routing-guard-nodes)
- [소스 라우팅 : BGP의 제한](#source-routing-limitations-of-bgp)
- [가상 경로 : 스카이와이어 네트워크 토폴로지 규모](#virtual-routes-skywire-network-topology-at-scale)
- [소스 라우팅 : 가상 경로, SONET 기술](#source-routing-virtual-routes-sonet-topology)
- [소스 라우팅 : 비대칭 연결](#source-routing-asymmetric-connectivity)
- [소스 라우팅 : 경로 검색](#source-routing-route-discovery)

<!-- /MarkdownTOC -->

## 소개

스카이와이어의 목표 : 

* 브로드밴드의 경쟁력을 높입니다. 현재 IPS 서비스를 대체합니다. last mile을 활용합니다.
* 커뮤니티가 사용자가 운영하는 인프라를 위한 ISP를 구축할 수 있습니다.

스카이와이어는 새로운 다크넷 프로토콜입니다.

* 낮은 대기율(TCP / IP만큼 빠르며 이론적으로는 기본 네트워크에서 더 빠름)
* 고성능(비디오, 파일 공유 및 고성능을 요구하는 응용 프로그램에 최적화)
* 개인정보보호 정책
* Wifi 지원(메쉬넷)
* Clearnet 지원 (Darknet / Overlay)

스카이와이어(Skywire)는 네트워크 배포에 대한 인센티브 및 불편한 문제를 해결합니다.

* 사용자는 네트워크 자원을 제공하고 스카이코인을받습니다.
* 사용자는 네트워크 자원을 사용하기 위해 동전을 소비합니다.

스카이와이어는 누구나 접근 가능합니다.

* 누구나 스카이와이어 노드에 연결할 수 있습니다.e
* 전역 개방형 액세스 메쉬넷(Meshnet)을 만드는 것이 목표입니다.

스카이와이어는 개인정보를 보호합니다.

* 노드를 통과하는 트래픽을 IP주소로 추적할 수 없습니다.
* 노드 전송 트래픽은 이전 및 다음 홉(hop)만 볼 수 있습니다.
* 제3자가 개별 패킷을 스트림 또는 사용자에 연결할 수 없습니다.
* 타사 및 전송 노드는 트래픽 내용을 읽을 수 없습니다.

## 라우팅 : 개요

스카이와이어 매쉬넷(Skywire meshnet)은 소스-라우트 저장- 전달(source-routed store-and-forward) 프로토콜을 사용합니다.

오버레이 네트워크(overlay network)의 핵심은 일련의 노드들에 있습니다.

* 각 노드는 공개 키 해시로 식별됩니다.
* 각 노드는 메시지를 수신 및 전송합니다.
* 노드는 트래픽 전송을 위해 코인을받습니다.

노드 'A'와 'C' 사이의 통신을 위해서는 노드 'B'를 거쳐야 합니다.:

* 노드 'A'가 노드 'B'에 연결하고 경로를 설정합니다.
* 노드 'A'가 노드 'C'로 경로를 확장합니다.
* 트래픽은 경로를 거쳐 'A'는 'C'에 도착하게 됩니다.

경로 `A -> B -> C -> D`:

* 노드는 경로의 이전 홉(hop)과 다음 홉(hop)만 알고 있습니다.
* 'C'는 메시지가 'B'를 거쳐서 'D'에 전달됨을 알 수 있습니다. 그러나 'C'는 'A'가 누구인지 알 수 없습니다.
* 'B'는 'A'가 그 경로은 원점인 것을 추측할 수 없습니다.
* 'C'는 'D'가 그 메시지의 최종 목적지인 것을 추측할 수 없습니다.
* 'B'와 'C'는 메시지의 내용을 읽을 수 없습니다.(종점(end-to-end) 암호화)
* 특정 메시지의 전송에 참여하지 않는 제3자는 메시지 내용에 대한 정보를 얻을 수 없습니다.(링크 계층 암호화)
*동일한 목적지에 대한 여러 경로의 여러 메시지가 번들로 제공되어, 제3자가 트래픽 분석을 수행 할 수 없습니다.

가장 간단히 구현할 수 있는 경로는 128 비트 프리픽스입니다.
각 노드는 프리픽스를 읽고, 패킷을 전송할 다음 노드를 결정하기 위해 테이블에서 조회를 수행합니다.

소스는 라우팅을 완벽하게 제어합니다.

* 각 노드는 자신의 필요에 맞게 라우팅 프로토콜을 독립적으로 업그레이드 할 수 있습니다.
* 소스는 VOIP 또는 게임의 서비스를 위해 대기 시간이 짧은 네트워크 경로를 위한 네트워크 경로를 최적화 할 수 있습니다.
* 소스는 비디오 및 파일 공유 응용 프로그램의 처리를 위해 네트워크 경로를 최적화 할 수 있습니다.
* 소스는 중복성, 대기 시간 및 처리량 감소를 위해 여러 경로를 묶을 수 있습니다.

일부 응용 프로그램은 다음을 위해 응용 프로그램 계층에 여러 개의 다중 경로를 제공합니다.:

* 개인 정보 보호(gatekeeper 노드, tor 타입 게이트웨이/anon 서비스)
* 처리량
* 대기 시간 감소
* 여분(redundancy)

이것은 스카이코인 오버레이 네트워크의 핵심입니다. 그것은 매우 간단하지만 매우 강력합니다.
기술 및 구현 세부 사항은 나중에 논의 될 것입니다.

스카이와이어는 패킷에 경로ID를 붙이는 간단한 프리픽스(prefixes)를 사용합니다.

* 라우팅은 매우 간단한 테이블 조회방식입니다.
* 패킷 당 오버 헤드는 일정하며 경로가 긴 경우에도 증가하지 않습니다.

설명:

* 목적지는 출발지의 신원을 알지 못한다. 식별자는 라우팅 레이어가 아니라 애플리케이션 레이어입니다. 신원은 공개키를 통해 확인되어야 합니다.
* 중개자 공격은 불가능합니다. 소스는 그들의 공개키를 통해 목적지를 확인할 수 있습니다.
* IPv4로부터 프라이버시가 크게 향상되어 패킷을 처리하는 모든 사람이 패킷의 목적지, 소스 및 내용을 볼 수 있습니다.
* ISP가 hot potato 라우팅을 사용하기 때문에 성능이 IPv4 / BGP보다 우수합니다.
* 종단 간 암호화는 패킷 인젝션 공격 및 스푸핑을 제거합니다. 스푸핑 트래픽은 연결 터널의 양쪽 끝에 개인키가 필요합니다.
* 암호화가 빠릅니다. 목표는 FPGA 하드웨어에서 10Gb/s, ARM에서 200Mb/s 입니다.

## 보상 : 지불 프로토콜

![스카이와이어 채굴자](https://i.imgur.com/2zj4CUV.jpg)

*[스카이와이어 "채굴자"](/statement/skywire-miner-hardware-for-the-next-internet/)*

이것은 스카이코인의 "채굴"과 동등하며 그들의 첫 번째 코인을 몇 명의 사용자가 얻을지 결정합니다.

전송에 대한 지불은 소스 노드의 ID를 나타내지 않아야 합니다. 스카이코인은 더 나은 프로토콜이 개발될 때까지 제3자를 통해 비공개 에스크로 지불을 사용합니다.

경로 상 각 노드와 원 노드는 트래픽을 기록합니다. 그들은 대역폭 지불을 주기적으로 계산합니다.

원 노드는 제 3의 공간 및 에스크로에서 동전을 보유하고 있습니다. A pseudonym account is created with the third party. Each node can verify reputation of the origin and payment ability through the third party, without learning identity of party. To the third party, each origin will appear as multiple unlinked pseudonym accounts. Each transit node will appear as multiple unlinked pseudonym accounts.

Small transactions will be settled internally, in off-blockchain transactions. The off-blockchain transactions can be withdrawn into a newly generated, never used before address once the balance exceeds a threshold (currently 1 Skycoin). This reduces blockchain bloat and encourages microtransactions to be performed off-blockchain.

## Source Routing: Link Layer Encryption

There is a default link layer encryption between hops and default end-to-end encryption. A typical application will use link layer encryption, end-to-end encryption and then appropriate application layer encryption.

Encryption between nodes should be fast. FPGA implementations must support 10 Gb/s operation at line speed. ARM processors must be able to support 250 Mb/s.

The current best candidate is ChaCha20 with ECC secp256k1 ephemeral key exchange.

ChaCha20 only uses simple arithmetic operations, is faster than AES for embedded devices and is more resistant to timing channel attacks than AES.

A modern CPU can perform 6000 secp256k1 ECDH operations per second. Session key rotation should be once per second or twice the round trip latency between nodes. There should be a separate key for each direction of communication.

The previous session key should be accumulated into the secret received via ECDH.

The session key, established through public key cryptography (ECC) is used to encrypt communications using a faster asymmetric encryption algorithm (AES, ChaCha20). This the basic link layer encryption between nodes

### Example Protocol: Nodes `A` and `B`

- Node `A` wants to generate session key for sending encrypted data to node `B`
- Node `B` has public key `P`, with private key `p`. `P` is a point on the ECC sep256k1 curve. `p` is a 256 bit integer. `P` is the basepoint b, raised to the power of p with the curve addition operation.
- Node `A` generates an ephemeral public key `Q`, with private key `q`. (Node `A` randomly generates a 20 byte integer. This is the private key `q`. Node `A` raises the base point to the power of `q`, to generate the private key `Q`, which is a point on the curve).
- Node `A` sends, `P`*`q` (the point on curve `P`, which is `B`’s public key, raised to power of `q`)
- Node `A` sends `P` to node `B`
- Node `B` receives `P` and computes `P*q`, Node `A` can compute `p*Q`, which are equal. This is the shared secret, which is hashed to generate session key.
- `P = b*q`, so `P*q` is equal to `(b*p)*q`.  `P*q = (b*p)*q = (b*q)*p = Q*p`, since `Q=b*q`. `A` knows `q,Q` and `P`, and `B` knows `p,P` and `Q`. So `A` and `B` can both compute `P*q` and `Q*p` and use this as their secret. However, a third party does not know the private keys `q` for `A` nor know the private key `p` for `B`, so a third party cannot compute this “secret” and therefore cannot read anything encrypted under the secret.
- Node `B` confirms receipt of the session key update. Node `A` begins transmitting under the new session key as soon as the confirmation is received from `B`.
- Node `A`, sends messages to node `B` by encrypting them using ChaCha20 using the session key, as the asymmetric encryption key.

### Possible Improvements:

- Frequent session key updates. ECDH key exchange every few seconds or minutes
- Hash old session key with new ECDH secret to generate new session key
- Add nonces to packets and hash secret into nonce to generate key for each message. Same key is never reused. Reduces impact of known plaintext attack.
- Eliminate known plain text in messages.
- Pad messages to multiples of 16 or 32 bytes

## IPv4 Gateway: Bypassing Existing ISPs

Many people have only a single choice for ISPs. This briefly describes how Skywire can increase competition

Some applications can run natively on the Skywire address space. Some applications such as Bittorrent, file syncing and communication applications strongly benefit from the Skywire infrastructure and will be modified to run natively on it.

Legacy applications, such as Netflix, Facebook, Twittter require a network gateway interfacing the Skywire overlay network with IPv4 and IPv6 networks.

A user chooses a Skywire gateway running on a server in a local colocation center. The users IPv4 traffic will be tunneled through the gateway (similar to a VPN). The users IP will appear as the IP of the gateway server . The server has a gigabit connection to multiple fast internet backbones, on providers which do not rate limit Netflix. The user has multiple choices of providers for Skywire IPv4 gateways. The gateway provider will be paid in Skycoin on a metered basis.

The Skywire node in the users home connects to the gateway over all possible routes. The Skywire node tunnels the IPv4 traffic from a router to the gateway in the colocation center. The IP address of the gateway node is the IP address that appears to the user.

### Example One

A user has a 10 Mb/s cable modem. They install a Skywire router. The router is plugged into their computer, into a Skywire Wifi node and into their cable model. The router is configured with Skywire as a IPv4 tunnel. They plug their computer into the router .

The Skywire wifi node connects to their neighbors Skywire node over wifi, which is connected to a 10 Mb/s cable modem. The neighbor also has a 200 Mb/s 5 GHz wifi with directional point-to-point antenna connected to a business running a Skywire wifi node down the street.

The users Skywire router does a recursive breadth first search for nodes with clearnet connectivity and establish routes over

* His cable modem
* Wifi -> his neighbors cable modem
* Wifi -> 5 GHz point to point -> 100/30 Mb/s business/fiber drop

The user will be able to access and aggregate bandwidth over all routes, in connecting to the IPv4 tunnel. In communities where aggregate bandwidth and reliability have reached a certain level, the user no longer needs the cable modem for connectivity.

### Example Two

The business down the street has a 100/30 Mb/s fiber drop with an SLA. The business pays a fixed rate for internet. Any bandwidth they do not use is lost. The business hooks up a Skywire router. The router has 3 ports. The first port is their WAN connection, the second port is their internal network, the third port goes to their Skywire wifi nodes on roof. The router buffers and prioritizes traffic on the internal network and allocates unused capacity to the Skywire traffic. The operator receives Skycoins for transit which, subsidizes the cost of the fiber drop.

## Skywire Daemon Services Architecture

* Each Skycoin node has a Secpk256k1 pubkey
* Each Skycoin node has a Skycoin address identifying it. The address is a hash of the node’s public key. This public key hash is the equivalent of an IP address on the network.
* Each Skycoin node has a connection pool of peer it is connected to. These can be peers over TCP, UDP clearnet connections, physical connections through direct Ethernet and Wifi peer (meshnet operation). A connection can also be a “virtual connection” which is tunneled through a physical or clearnet connection and will be described later.
* Each connection instance with a peer has “channels”. A channel is a 16 bit integer which is similar to a “port” in TCP.
* All messages sent and received have a 32 bit length prefixed and 16 bit channel.
* Channel 0 is reserved for communication between Skywire Daemons,  exposing meta-information about the services running on the Daemon and other data required for network operation.
* A Skywire daemon may expose “services” on a channel. A service is a process that handles data messages received on a channel and originates data messages addressed to remote peers and services.

### Example Service: Blockchain Sync

*This example is refers to a Golang implementation, but the daemon architecture is language agnostic.*

You want to sync two different personal block chains of people with public keys A and B. You initiate two “blockchain sync service” instances, configure them with the respective public keys and associate them with the Skycoin Daemon. These services run on your local daemon, each on a particular channel.

#### Finding Peers

The blockchain sync daemons the hash the public key and do a DHT (Distributed Hash Table) lookup to find other peers syncing the blockchain. Once peers are found, the peers can be introduce each other to additional peers through PEX (Peer Exchange).

#### Sending and Receiving Messages

Services on creation register a list of messages they respond to and can send. Messages are Golang structs. The message struct data is filled out and then sent. The data arrives and the .Handle() method is called on the corresponding message struct.

## Multi-Home Routing and Link Aggregation

If you have a 2 Mb/s cable modem and your neighbor has a 2 Mb/s cable modem and each of you are running Skywire nodes, then your Skywire node can connect to his node and aggregate the bandwidth across both connections. Packets may now take routes through your cable modem and routes through his cable modem. The cable modems are the choke point. To get a 4 Mb/s connection, traffic has to pass in parallel paths through both modems.

Applications like Bittorrent will be able to aggregate bandwidth across all available connections, because they natively open up a large number of connections, which will take district routes.

## Meshnet Routing: Store and Forward

For nodes at the edge of the network communicating over mesh, there are a few issues.

If you have an eight hop network over Wifi and 50% of packets drop on each hop, then only 1 in 256 packets will make it through. Packet drop is normal on Wifi, but traditional TCP treats packet drop as congestion and throttles the connection speed back.

At the network edge, Skywire will use store and forward along routes. This imposes a memory requirement on Skywire nodes, but significantly improves network performance.

For the route `A->B->C`

* Each route has a buffer.
* Each node keeps sending the messages until they are received and acknowledged.
* If the Buffer from `B->C` is full for the route, then `A` will know this and will stop transmitting data until the sent data has been acknowledged there is room in the buffer.

Therefore there are two acknowledgements between nodes at the link layer. One acknowledgement is an affirmative acknowledgement that transmitted data segments were received. Another is an acknowledgment that data from the buffer has been sent to and acknowledged by the next node in the route.

## Store and Forward: Capacity Utilization

In traditional IP networks, as network links are utilized towards capacity the efficiency drops. A network running at 80% capacity faces the risk that a short term burst of data causes a router to go over capacity and network packets are dropped.

TCP interprets dropped packets for any reason as congestion and throttles back speed. The dropped packets also require retransmission under TCP and introduce latency as the application waits for timeout and retransmission before it can process the rest of the packet stream.

With store and forward operation, the route buffers fill up and then nothing happens. When the buffers fill, the incoming node stop sending data until notified of space in the buffer.

This store and forward operation is especially important for practical Wifi meshnets. There are only three non-overlapping channels in the 2.4 GHz band. Packet loss increases very quickly and very early compared to the bandwidth saturation point for a Wifi networks. Wifi packet loss is inevitable and does not reliably indicate congestion or capacity limits.

Store and forward allows us to run the Wifi nodes at full capacity and saturate all available bandwidth, without triggering TCP congestion controls.

Practical networks will require:

* Software Defined Radio
* MIMO
* Beam Forming
* Directional Antennas
* Cooperative temporal and geophysical coordination of transmission time, broadcast power and frequency usage
* 801.11af whitespace frequencies

## Store and Forward: Examples

Each node, for each route keeps track of:

* Buffer size for receiving node for route
* Predicted buffer size (acked and unacked datasegments transmitted)
* Acked buffer size
* Offset, size and sequence of each transmitted message that has not been acked
* Circular buffer of bytes of outgoing datagrams that have not received an ack

A data segment on the link layer may contain concatenated messages, from multiple routes addressed to the same node. This frustrates traffic analysis and improves performance by allowing larger datagrams on networks which support higher MTUs.

For each transmitted message, there are two acks. The first ack is that the datagram has been received by the next node in route. This is an ack for the datagram, which may contain multiple messages, each corresponding to different routes. After receiving this ack, the node no longer needs to retain the datagram. If the datagram is not acked, then it needs to be resent.

The second ack are updates about remaining free bytes in the incoming buffer for a route. If the free bytes in the buffer for a route is large enough, then additional messages for that route can be transmitted.

Another possible approach, maintains a buffer per sender instead of per route, with the receiver sending block messages to the sender for congested routes. This reduces the number of route hash lookups required by sender and is something that may have to be experimented with.

### Example of normal operation

Route: `A->B->C`

* B has 1024 KB buffer for route
* A sends 512 KB to B
* B Acknowledges the 512 KB to A
* < A receives the Acknowledgement (and clears first 512 KB, no longer needs to be stored) >
* B forwards 512 KB to C
* C acknowledges receipt of the 512 KB
* C acknowledges to A that the 512 KB has been forwarded

### Example with congestion

Route: `A->B->C`

* B has 1024 buffer for route
* A sends 512 KB to B
* A sends 256 KB to B
* A sends 256 KB to B
* < A stops sending because pending, is already enough to fill buffer at B >
* B acknowledges to A the receipt of 512 KB and 512 KB
* B sends 256 KB to C
* C acknowledges receipt of 256 KB to B
* B acknowledges to B, forwarding of 256 KB to A
* < A can now send, up to 256 KB additional KB >


Data is assumed to be received in the order sent for Wifi and direct ethernet connection

### Example with packet loss

Route: `A->B->C`

* B has 1024 buffer for route
* A sends 512 KB to B
* A sends 256 KB to B
* B acks the 256 KB
* A infers that the 512 KB was not received
* A retransmits the 512 KB
* B acks the 512 KB
* < B can now continue sending stream in order to C >

## Store and Forward: Bandwidth Latency Product

In store and forward a storage requirement is imposed on the transmitting node equal to the product of the round trip latency and the transmission rate times the round trip latency. 1 GB of ram is enough for 8000 ms round trip latency at 1 Gb/s transmission rate.

Store and forward should be default, but optional.

## Store and Forward: Capacity Utilization, Quality and Service

Video, Audio and file downloads are buffered. Absolute averaged throughput over a time window of seconds matters, while latency is irrelevant. Other traffic such as website requests, video game and voip is real time and should be delivered as quickly as possible.

With two quality of service levels, “Real Time” and “Bulk” we can transmit VOIP, website and `video game traffic first, reducing latency for this traffic. Latency insensitive traffic such as video, music and file sharing would only flow over link after real time traffic buffer is empty.

We are able to utilize links at near 100% of capacity while, lowering latency for real time traffic. Therefore we propose supporting two quality of service levels for routes.

## Source Routing: Multi-Route Mobile Connectivity

If connections between nodes are stable, low latency and have high bandwidth then a single route is sufficient for most applications. Some applications like Bitorrent, open a large number of connections and natively can use bandwidth across all available routes.

If the links between nodes are slow, unreliable or connectivity is changing, reliability and performance requires traffic to be multiplexed over multiple redundant routes.

If a Skywire node running on a cell phone is in a car driving down the street, the networks that are accessible will change. Network nodes will come into range and other network nodes will leave range. The node should have continuous connectivity at the application layer, even as the physical connections are created and destroyed.

One approach is choosing a set of reliable nodes on the network backbone as termination points for a route and then proxying the traffic through these nodes, over a set of multiple short term routes.
Source Routing: Multi-Route Reliability

If links are unreliable or have highly variable latency, it is desirable to encode application data over multiple paths, such that the data can be recovered if data from any of the paths is received. Fountain coding and other encoding methods exist which may be applicable here.

## Source Routing: Guard Nodes

For privacy, if a user wants to further weaken linkability between their Skywire node address (public key hash) to their IP address, they can destinate a fixed set of nodes that are advertised as being transit points for traffic destined for their address or act as required nodes on a route from their address.

## Source Routing: Limitations of BGP

Border Gateway Protocol, the current dominant routing protocol, handles the routing problem by not keeping any state for packets. Instead BGP, allows each network to create a series of ad-hoc rules for each of its routers which look at the source and destination of a packet and decide which network interface to forward the packet to. Routers message each other with connectivity information and another routing algorithm is used for routing within a network domain.

BGP is designed to interface a series of independent autonomous networks. BGP has a homogeneity assumption, the routing within an autonomous domain is assumed to be centrally managed and highly reliable with homogenous routing within the domain. Mesh network and community ISPs will be ad-hoc with heterogeneous device connectivity and routing.

Connectivity in mesh networks, ad-hoc configurations and densely interconnected networks with redundant multi-home routing paths completely violate the hierarchical assumptions BGP.

BGP has several issues that a next gen protocol should address:

* BGP is not self configuring. BGP based networks require extensive technical expertise to configure and operate
* BGP systems often require manual configuration to route around damage and are not resilient against bad configurations
* BGP requires manual creation of ad-hoc route filtering rules and increasing complexity for networks with multi-home connectivity
* BGP networks require highly centralized planning
* The NSA has exploited flawed in BGP to route targeted traffic to interception points
* The assumptions of BGP are becoming increasingly strained, especially for ad-hoc, mesh and mobile networks
* The hierarchical, single path assumptions of BGP make implementation of multi-homing and other next-gen networking requirements extremely difficult
* BGP suffers severe issues when network links are unreliable, such as route flapping.
* BGP routing table size grows exponentially as interconnected subnetworks proliferate.
* Multihoming causes a massive explosion in BGP routing table size.
* BGP has difficulty with load balancing and multi-home routing. BGP limits the ability in practical networks to take advantage of parallel connectivity between locations.
* BGP creates an incentive for ISPs to dump network traffic on to other networks as quickly as possible (“Hot Potato Routing”), reducing performance and increasing latency

There is no alternative to BGP. BGP is the best solution within its design constraints.

The successor to BGP must:

* Be non-hierarchical
* Be self-configuring (zero-conf)
* Operate well with dense ad-hoc, redundant interconnection between networks

## Virtual Routes: Skywire Network Topology at Scale

The Skywire routing implementation requires a node to maintain information for each route that passes through it. Individual nodes are unable to handle hundreds of thousands of individual routes and scalability is achieved through another mechanism.

Skywire is experimenting with a non-hierarchical, self organizing routing that natively supports multihoming and non-hierarchical network topographies while scaling efficiently.

Skywire minimizes network diameter as the network scales through the use of virtual routes. Virtual routes allow thousands of connections to be bundled over a high bandwidth backbone connection with the overhead of a single route.

A “virtual route” creates a tunnel over an existing route:

`A -> B -> C -> D`

The virtual route appears as A->D. B and C may be high bandwidth long distance connections. B and C only incur the overhead of a single route, while A and D incur the overhead of maintaining the routes on the A->D tunnel.

The virtual route may contain traffic from hundreds of bundled routes from A to D, while B and C only experience overhead of a single route. The virtual route may further, bundle multiple redundant network paths between the origin and destination for performance, throughput and redundancy.

Virtual routes allow network capacity to be clustered roughly hierarchically with nodes at each layer having a constant fan in and overhead.

Nodes at the network edge feed into aggregation nodes. Edge aggregation nodes are connected to high bandwidth intradomain transit and feed into gateway nodes which interface between networks. Gateway nodes feed into high bandwidth and long-haul transit.

Virtual routes are a representation of existing interdomain routing relationships, which natively support:

* Non-hierarchical routing (data centers)
* Multiple-homing
* Dense network interconnection between domains at different levels of hierarchy
* Multi-path routing within and between network domains

Virtual routes obey a triangle equality. If the cost of a route A->B, is C(A->B) then

`C(A->B->C) >= C(A->B) + C(B->C)`

Origin preference for low latency, low cost, and low hop routes, creates economic incentives to create an efficient network topology. The network is non-hierarchical and self-organizing. The virtual routes that are created are route summarizations that naturally reflect the flow of traffic.

In BGP, networks try to get rid of traffic as quickly as possible (hot potato routing). In Skywire, networks compete to provide transit (to receive coin incentives). Skywire clients will preference, low cost, low hop count and low latency routes. Networks with direct long haul capacity between source and destination have lower latency and lower hop count and therefore receive preference.

For efficiency, the bandwidth capacity and fan-in (number of routes each virtual route is bundling) at each level of the network hierarchy must be constant, in order to achieve a constant network diameter and logarithmic routing table growth in the number of hosts.

## Source Routing: Virtual Routes, SONET Topology

A multiple-input, multiple-output virtual route, may be physically implemented as a SONET ring, with Skywire nodes in each city the SONET topology passes through. The Skywire nodes act as a gateway router between the Skywire network and the SONET topology.

Nodes are able to queue up large datagrams concatenating multiple messages from the same source to the same destination for efficiency.

The message enters the Skywire node of the SONET ring at a colocation center in one city. The message destination or route is read and the message is encoded for transport over the SONET segment. The message arrives at the destination Skywire node on the SONET segment and continues on its path.

A multiple input, multiple output virtual route is therefore a list of Skywire nodes, with a transit cost, describing a SONET ring or fully connected topology, where any node in list has transit to any other node in the list.

## Source Routing: Asymmetric Connectivity

Next gen wifi systems will have 4x4 and 8x8 antennas in a phased array MIMO arrangement. Such systems are able to project highly focused directional beams. These systems significantly increase the power and signal strength at the receiver, but do not symmetrically improve antenna gain for return signals.

Similarly, a high powered, amplified wifi signal through a directional antenna may be received at a site fifteen miles away, but reception of the signal from the site cannot similarly be amplified as easily as power can be boosted in transmission.

We propose, Asymmetric routes, for situation where messages can be received by a node, but where the node cannot directly communicate back. In an asymmetric route confirmation messages are relayed over the network by a route, enabling full utilization of asymmetric connectivity over one way communication channels.

Situations where this will become increasingly relevant

* Rural SONET arrangements with amplified Wifi over directional antennas
* Urban connectivity between highly directional and non-directional antennas broadcasting at the same power levels
* Concrete penetration in 802.11af systems
* Non-line of sight LiFi propagation can transmit over 200 Mb/s but its highly asymmetrical
* RONJA type Li-Fi systems have theoretical capacity limits over 10 Gb/s line-of-sight and there is cost/setup advantage for asymmetrical connectivity

Utilizing asymmetric connectivity and routes allowing only one way direct data transmission between nodes has several advances, especially for rural developments and reducing cost of integrating high capacity of next-gen technologies.

## Source Routing: Route Discovery

IPv4 gateway and meshnets for community ISPs, only require breadth first search over paths to clearnet connectivity. The best, most reliable, highest throughput routes have very small depth. Therefore we consider routing solved for this case. Will look at general routing later.
