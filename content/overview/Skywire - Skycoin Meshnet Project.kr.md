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

원 노드는 제 3의 공간 및 에스크로에서 동전을 보관하고 있습니다. 익명 계정은 서드파티(제3자)와 함께 생성됩니다. 각 노드는 원 노드의 정보를 참조하지 않고 서드파티를 통해 원 노드 및 지불능력에 대해 확인할 수 있습니다. 서드파티에서 각 원본 계정은 여러 개의 연결되지 않은 익명 계정으로 표시됩니다. 각 중계 노드는 여러 개의 연결되지 않은 익명 계정으로 표시됩니다.

소규모 거래는 블럭체인 트랜젝션 외부에서 내부거래로 처리될 것입니다. 오프-블록 체인 트랜잭션은 잔고가 최소값(현재 1 스카이코인)을 넘는 경우, 이전에 사용되지 않은 새로 생성된 주소로 출금할 수 있습니다.  이것은 블록체인의 팽창을 감소시키며 마이크로트랜잭션을 블록체인 외부에서 수행할 수 있도록 합니다.

## 소스 라우팅 : 링크 계층 암호화

이것은 홉과 기본 종단(end-to-end) 암호화 간의 기본 링크 계층 암호화입니다. 일반적인 응용 프로그램은 링크 계층 암호화, 종단 간 암호화 및 적절한 응용 프로그램 계층 암호화를 사용합니다.

노드 간 암호화는 빠르게 수행됩니다. FPGA 실행은 10Gb/s 회선 속도를 지원해야 합니다. ARM 프로세서는 250Mb/s를 지원할 수 있어야 합니다.

현재 가장 적합한 후보는 ECC secp256k1 임시 키 교환방식을 사용하는 ChaCha20입니다.

ChaCha20은 단순한 산술 연산만을 사용하며, 임베디드 장치의 경우 AES보다 빠르고, AES보다 시차공격(timing channel attacks) 방어가 더 강력합니다.

최신 CPU는 초당 6000 secp256k1 ECDH 작업을 수행 할 수 있습니다. 세션 키 순환은 초당 한 번 또는 노드 간의 라운드 트립 대기 시간의 두 배가 되어야 합니다. 각 방향의 통신을 위해 별도의 키가 있어야 합니다.

이전 세션 키는 ECDH를 통해 전달받은 비밀데이터에 축적되어야 합니다.

공개키 암호화(ECC)를 통해 설정된 세션키는, 보다 빠른 비대칭 암호화 알고리즘(AES, ChaCha20)을 사용하여 통신을 암호화 하기 위해 사용됩니다. 
이것은 노드 간의 통신을 위한 기본 계층 암호화 기법입니다.

### 프로토콜 예제 : 노드 'A' 와 'B'

- 노드 `A`가 암호화 된 데이터를 노드 `B`에 보내기 위한 세션키를 생성하려고합니다.
- 노드 `B`는 개인키 `P`와 함께 공개키 `P`를 가지고 있습니다. `P`는 ECC sep256k1 경로의 한 지점입니다. `P`는 256 비트 정수입니다.
`P`는 기준점 b이며, 경로 추가 작업 시 생성됩니다.
- 노드 `A`는 개인키 `q`와 임시 공개키 `Q`를 생성합니다. (Node `A`는 무작위로 20바이트 정수를 생성합니다. 이 키는 개인키 `q`입니다. 노드 `A`는 기준점을 `q`지점으로 높이고, 개인키 `Q`를 생성하는데, 이것은 경로의 한 지점입니다.)
- 노드 `A`를 `P`*`q`로 전송합니다.(구간 `P`의 포인트, `B`의 공개키, `q`의 파워를 높여줍니다.)
- 노드 `A`는 노드 `B`로 `P`를 전송합니다.
- 노드 `B`는 `P`를 수신받아 `P*q`를 계산하고, 노드 `A`는 `p*Q`를 계산할 수 있습니다. 그리고 그 계산값은 동일합니다. 이것은 해시 처리된 세션키를 생성하기 위해 공유된 비밀입니다.
- `P = b*q`, 따라서 `P*q'와 '(b*p)*q`는 같습니다. `A`는 `q,Q`와 `P`를 알고 있으며, `B`는 `p,P`와 `Q`를 알고 있습니다. 따라서 `A`와 `B`는 
그들의 비밀방식을 사용하여 `P*q`와 `Q*p`를 계산할 수 있습니다. 그러나 제3자는 `A`의 개인키 `q`나 `B`의 개인키 `p`를 알 수 없는데, 
제3자는 "비밀방식"을 계산할 수 없으며 또한 비밀방식으로 암호화 된 그 어떤 정보도 읽을 수 없기 때문입니다.
- 노드 `B`는 세션 키 업데이트의 수신을 확인합니다. 노드 `A`는 `B`로부터 확인 받은 즉시, 새로운 세션 키로부터 전송을 시작합니다.
- 노드 `A`는 노드 `B`로 세션 키를 사용한 ChaCha20라는 비대칭 암호화 키로 암호화하여 메시지를 전송합니다.

### 가능한 개선 사항 :

- 잦은 세션 키 업데이트. 몇 초 또는 몇 분마다 ECDH 키 교환.
- 새로운 세션 키를 생성하기 위해 새로운 ECDH 암호화를 이전 세션키로 해시해야 합니다.
- nonce를 패킷에 추가하고 secret을 nonce에 해시하여 각 메시지의 키를 생성합니다. 같은 키는 결코 재 사용되지 않습니다. 알려진 평문 공격의 영향을 
줄입니다.
- 메시지에서 알려진 평문을 제거합니다.
- 패드 메시지를 16 또는 32 바이트의 배수로 설정합니다.

## IPv4 게이트웨이 : 기존 ISP 우회

많은 사람들이 단 하나의 ISP를 사용하고 있습니다. 이것은 스카이와이어가 어떻게 시장 경쟁력을 높일 수 있는지 간단하게 설명할 수 있습니다.

일부 응용 프로그램은 스카이와이어 주소 공간에서 원활하게 실행할 수 있습니다. 비트토렌트(Bittorrent), 파일 동기화 및 통신 애플리케이션과 같은 일부 애플리케이션은 스카이와이어 인프라 구조를 강력하게 활용하며 원활하게 실행될 수 있도록 개선될 것입니다.

Netflix, Facebook, Twitter와 같은 기존 응용 프로그램은 스카이와이어 오버레이 네트워크를 IPv4 및 IPv6 네트워크와 연결하는 네트워크 게이트웨이가 
필요합니다.

사용자는 지역 센터의 서버에서 실행 중인 스카이와이어 게이트웨이를 선택합니다. 사용자의 IPv4 트래픽은 게이트웨이를 통해 이동합니다.(VPN과 유사) 
사용자 IP는 게이트웨이 서버의 IP로 나타납니다. 서버는 Netflix 전송속도 제한율이 없는 제공 업체를 통해 다중 고속 인터넷 백본을 위한 기가비트 
연결을 설정합니다. 사용자는 스카이와이어 IPv4 게이트웨이를 제공하는 업체들 중에서 다양한 선택을 할 수 있습니다. 게이트웨이 제공업체에게 사용량 
기준으로 스카이코인이 지급될 것입니다.

사용자 개인의 스카이와이어 노드는 가능한 모든 경로를 통해 게이트웨이에 연결됩니다. 스카이와이어 노드는 라우터에서 지역 센터의 게이트웨이로 IPv4 
트래픽을 전송합니다. 게이트웨이 노드의 IP 주소는 사용자에게 표시되는 IP 주소입니다.

### 예제 1

사용자는 10 Mb/s 케이블 모뎀을 사용합니다. 그들은 Skywire 라우터를 설치합니다. 라우터는 컴퓨터, 스카이와이어 Wifi 노드 및 케이블 모델에 
연결됩니다. 라우터는 스카이와이어의 IPv4 터널로 구성됩니다. 그들은 개인용 컴퓨터를 라우터에 연결합니다.

스카이와이어 wifi 노드는 10Mb/s 케이블 모뎀에 연결된 wifi를 통해 이웃 스카이와이어 노드에 연결됩니다. 이웃 역시 200Mb/s 5GHz Wi-Fi와 점-대-점 
안테나가 있으며, 이것은 근처에 위치한 스카이와이어 무선랜 노드 사업장과 연결되어 있습니다.

사용자의 Skywire 라우터는 clearnet 연결을 통해 노드를 먼저 검색하고 경로를 설정하는 작업을 반복합니다.

* 사용자의 케이블 모뎀
* Wifi -> 이웃의 케이블 모뎀
* Wifi -> 5 GHz 점 대 점 -> 100/30 Mb/s 비지니스/필드 소멸

사용자는 IPv4 터널에 연결하여 모든 경로에서 대역폭에 접속 및 집계 할 수 있습니다. 총 대역폭과 신뢰성이 일정 수준에 도달한 커뮤니티에서, 
사용자는 더 이상 연결을 위한 케이블 모뎀을 필요로 하지 않습니다.

### 예제 2

근처에 100/30 Mb/s fiber drop과 SLA를 가진 사업장이 있다. 사업장은 인터넷 사용을 위해 정해진 요금을 지불합니다. 사용하지 않는 대역폭은 모두 손실됩니다. 사업장은 스카이와이어 라우터를 연결합니다. 라우터에는 3 개의 포트가 있습니다. 첫 번째 포트는 WAN 연결이고, 두 번째 포트는 내부 네트워크
이며, 세 번째 포트는 옥상에 있는 스카이와이어 Wi-Fi 노드로 연결됩니다. 라우터는 내부 네트워크의 트래픽을 버퍼링하고 우선 순위를 지정하며 
사용되지 않는 용량을 스카이와이어 트래픽에 할당합니다. 운영자는 전송을 위해 쓰이는 fiber drop 비용에 대한 보조금으로써 스카이코인을 받는다.

## 스카이와이어 데몬 서비스 구조

* 각 스카이코인 노드에는 Secpk256k1 공개키가 있습니다.
* 각 Skycoin 노드에는 식별을 위한 스카이코인 주소가 있습니다. 주소는 노드의 공용키 해시입니다. 이 공개 키 해시는 네트워크의 IP 주소와 동일합니다.
* 각 스카이코인 노드들은 피어가 연결된 연결 풀이 있습니다. 이것들은 TCP, UDP clearnet 연결, 직접적인 이더넷 및 Wifi 피어(메쉬넷 작업)를 통한 
물리적 연결을 통해 피어가 될 수 있습니다. 연결은 물리적 연결 또는 clearnet 연결을 통해 전송되는 "가상 연결"일 수도 있으며 나중에 다시 설명됩니다.
* 피어와 연결된 각 연결 인스턴스에는 "채널"이 있습니다. 채널은 TCP의 "포트"와 유사한 16 비트 정수입니다.
* 주고 받은 모든 메시지에는 32 비트 길이의 접두사와 16 비트 채널이 있습니다.
* 채널 0은 스카이와이어 데몬 간의 통신을 위해 예약되어, 데몬에서 실행되는 서비스에 대한 메타 정보와 네트워크 작동에 필요한 기타 데이터를 
노출합니다.
* 스카이와이어 데몬은 채널에 "서비스"를 노출시킬 수 있습니다. 서비스는 채널에서 수신된 데이터 메시지를 처리하고 원격 피어 및 서비스로 보내지는 
데이터 메시지를 전송하는 프로세스입니다.

### 서비스 예 : 블록 체인 동기화

*이 예제는 Golang 구현을 나타내지만, 데몬 구조는 특정 언어에 제한적이지 않습니다.*

당신은 두 개의 서로 다른 개인 블록체인을 공개키 A 및 B와 동기화 하려고 합니다. 당신은 우선 두 개의 "블록체인 동기화 서비스" 인스턴스를 시작하고, 
각각의 공개 키를 구성하여 스카이코인 데몬과 연동시킵니다 이 서비스는 당신의 로컬 데몬(각각의 개별적인 채널)에서 실행됩니다.

#### Peer 찾기

블록 체인 동기화 데몬은 공개키를 해시처리 DHT(분산된 해시 테이블) 조회를 수행하여 블록체인을 동기화하는 다른 피어를 찾습니다. 일단 피어가 발견되면 피어는 PEX(피어 교환)를 통해 다른 피어에게 접근할 수 있습니다.

#### 메시지 송/수신

레지스터 등록 서비스는 송/수신 가능한 메시지 목록을 생성할 수 있습니다. 메시지는 Golang 구조입니다. 메시지 구조체 데이터는 생성되고 전송됩니다. 
데이터가 도착하고 .Handle () 메서드가 해당 메시지 구조체에 호출됩니다.

## 다중 홈 라우팅 및 링크 집계

만약 당신이 2Mb/s 케이블 모뎀을 가지고 있고 이웃이 2Mb/s 케이블 모뎀을 가지고 있으며 각각 스카이와이어 노드를 실행하고 있다면,
당신의 스카이와이어 노드를 이웃의 노드에 연결할 수 있으며, 쌍방 연결에 대한 대역폭을 집계할 수 있습니다. 이제 패킷은 케이블 모뎀을 통해 경로를 
설정하고 케이블 모뎀을 통해 라우팅 할 수 있습니다. 케이블 모뎀은 초크 포인트입니다. 4 Mb/s 연결을 얻으려면, 트래픽이 두 모뎀을 통해 병렬 경로로 
전달되어야 합니다.

비트 토렌트(Bittorrent)와 같은 응용 프로그램은 사용 가능한 모든 연결에서 대역폭을 집계 할 수 있는데,
기본적으로 지역 루트를 통해 많은 수의 연결(커넥션)을 생성하기 때문입니다.

## 메쉬 라우팅 : 저장 및 전송

메쉬를 통해 통신하는 네트워크의 가장자리에 있는 노드의 경우 몇 가지 문제가 있습니다.

8홉 네트워크는 Wifi를 거쳐가며 각 홉에서 패킷의 50 %가 탈락되고, 256 패킷 중 1패킷만 통과하게됩니다. 패킷 탈락은 Wifi에서는 정상이지만, 
일반적인 TCP는 패킷 탈락을 혼잡으로 처리하고 연결 속도를 다시 조절합니다.

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

## 소스 라우팅 : 경로 검색

IPv4 gateway and meshnets for community ISPs, only require breadth first search over paths to clearnet connectivity. The best, most reliable, highest throughput routes have very small depth. Therefore we consider routing solved for this case. Will look at general routing later.
