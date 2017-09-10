+++
title = "스카이코인 AMA 기록(ark.io에서 개최)"
tags = [
    "Ask the Developers",
]
date = "2017-08-01"
categories = [
    "Ask the Developers",
    "Statement",
]
description = "스카이코인 AMA기록은 ark.io/slack/에서 확인할 수 있습니다.(2017-07-02일 부터)"
+++

*원본은 2017년 7월 2일자[ark.io 슬랙(https://ark.io/slack/)에 있습니다.*

*synth는 이 AMA에서 스카이코인의 대표자로 참석했습니다.*

**boldninja**
모두 SkyCoin.net의 @synth를 따뜻하게 환영해 주시기 바라며, AMA를 시작하겠습니다.

**synth**
안녕하세요.

**mike**
synth 안녕하세요.

**jakethepanda**
헤이 @synth

**thrice.pi**
헤이 synth

**dr10**
안녕하세요.

**boldninja**
이제 시작할 수 있겠군요. - 모두 어떻게 할 지 알고 있겠죠. 그에게 답변할 수 있는 시간을 주세요.
(그가 답변할 수 있도록 백로그에 2-3개의 질문만 남겨주세요.) 

**dr10**
당신의 어떻게 - 쉽고 간단한 단어로 - 스카이코인의 장점을 언론(매거진)과 암호화코인을 모르는 사람들에게 홍보할 것입니까?

**mgaruccio**
메쉬넷에 대해 간단히 설명해 줄 수 있나요? 이것은 노드 간의 mpls 네트워크입니까? 아니면 더 깊은 무언가가 있는 것입니까?

**michaelthecryptoguy**
안녕하세요. @synth

**tranzer**
안녕하세요.synth. 나는 질문이 있습니다. CMC에 따르면 이 코인은 현재 일부분만 사용할 수 있기 때문에 몇몇 비활성 지갑들(cold wallets)에 있는 
코인들은 거래할 수 없나요?
스카이코인이 가지고 있는 가장 독특한 특징은 무엇이라고 생각하십니까?

**synth**
매우 답변하기 어렵군요. 왜냐하면 스카이코인은 매우 큰 프로젝트이며 우리는 이미 6년 이상의 개발기간을 거쳤습니다.
프로젝트의 각각 다른 파트들은 각자 다른 목표를 가지고 있습니다.
암호화, 코인파트의 목표는 기존 합의 알고리즘의 문제점을 해결하는 것입니다.
초 당 300건 이상의 트랜젝션을 수행할 수 있기 때문에, 분 당이 아닌 초당 트랜젝션(신용카드보다 빠름) 수행, 채굴자 제거, 블럭 보상 제거
(인플레이션 제거) 그리고 51%공격 제거
및 채굴로 인해 발생되는 다른 문제점들도 해결할 수 있습니다.
다음으로 메쉬넷, 분산 VPN 프로토타입 같은 다른 repo들 및 실험프로젝트가 https://github.com/skycoin에 있습니다.
사람들은 트래픽을 전달하기 위해 코인을 지불할 것입니다. 또한 분산 소셜 미디어 어플리케이션의 프로토타입을 
P2P(peer to peer) 데이터 복제 및 다른 실험적인 프로젝트를 활용하여 제작하고 있습니다.
차세대 인터넷을 위한 변조 불가능한 데이터 구조를 연구하고 있습니다. 그 중 일부는 매우 원론적입니다.

**dr10**
네트워크 컨센서스 알고리즘 Obelisk는 어떻게 작동하며 Proof of Work 및 Stake of Proof와 같은 널리 알려진 알고리즘과 어떻게 다릅니까?

**mgaruccio**
그래서 현재 얼마나 많은 플랫폼이 존재합니까? 제가 원한다면 플랫폼에 앱을 만들 수 있습니까?

**mike**
진행 속도와 관련하여 현재 자금 지원, 인력, 현재 사용 가능한 기술과 같은 것들 중 가장 중요한 제한 요소는 무엇입니까?

**synth**

> 메쉬넷에 대해 간단히 설명해 줄 수 있나요? 이것은 노드 간의 mpls 네트워크입니까? 아니면 더 깊은 무언가가 있는 것입니까?

실제로는 메쉬넷이 아닙니다. 소프트웨어로 정의된 네트워킹이며, 단순한 메시넷보다 훨씬 강력합니다. 
그것의 새로운 유형의 네트워킹이며,  새로운 완전한 프로토콜 및 네트워킹 네임 스페이스로써, 현재의 인터넷에서 독립적입니다.
이것은 기존의 인터넷이 hot potato 라우팅을 하는 동안 소스 라우팅을 지원하므로, 최적의 대기시간이 필요하지 않습니다.
이것은 멀티홈(multi-homing)을 지원합니다. IPv6는 아닙니다.(기가비트 또는 테라 비트 네트워킹 및 다중 중복 대역폭 경로가있는 경우에는 중요합니다.)
링크 층과 종단 간 기본 복제 방지 암호가 있습니다.; 그래서 모든 것이 현재의 인터넷과 달리 기본적으로 암호화됩니다. 
저장 및 전송 네트워킹을 갖추고 있으며 이것은 아프리카 또는 다른 열악한 조건, 대기 시간이 몇 분 또는 몇 시간이며 패킷 손실이 과도한 상황 등 
기존 프로토콜이 신뢰성을 보장할 수 없는 곳에서도 작동합니다. 이것은 IPv4/IPv6 또는 TCP/ip보다 훨씬 강력합니다
개인정보보호가 향상되었습니다. 
한 패킷이 10 홉의 하나의 경로를 가지고 있는 경우, 각 홉은 경로의 이전 노드와 다음 노드만을 알고 있습니다. IPv4와 달리 각 패킷이 
출발지와 목적지를 제공합니다. 
개인정보보호 수준은 현재 인터넷에 존재하지 않는 것입니다. 
IP 주소는 공개키로 대체되며 그 누구도 대상을 식별하는 공개키의 개인키를 모른다면 목적지의 트래픽을 읽을 수 없습니다.
시스템은 제3자 및 인증기관의 인증을 필요로하지 않습니다. 
이 설계는 혁명적입니다.

> CMC에 따르면 이 코인은 현재 일부분만 사용할 수 있기 때문에 몇몇 비활성 지갑들(cold wallets)에 있는 코인들은 거래할 수 없나요?
이 코인은 각각 1백 만 개의 코인을 보유하고 있는 100개의 계정에 묶여있습니다. 그리고 이것은 순차적으로 풀리게 됩니다.
복잡한 잠금절차와 새로운 코인을 발급받기 위해서는 익명의 동의와 개발자 그룹 간 공유된 비밀이 필요합니다.
공유된 비밀 그룹에 있는 누구나(소멸된 NXT의 문제를 막기 위해) 더 많은 코인의 분배를 차단할 수 있습니다.
따라서 분배의 분배를 위한 설계는 어려우므로, 코인 분배가 승인되기 전에 타당한 이유 또는 정당성이 있어야 했습니다.

**mike**
무선 스카이와이어(위에서 설명한 프로토콜의 이름)노드를 작동하는데 필요한 하드웨어 요구사항은 무엇입니까?

**arc-over-water**
제 생각에는 nex가 괜찮다고 생각해요.

**synth**

> 네트워크 컨센서스 알고리즘 Obelisk는 어떻게 작동하며 Proof of Work 및 Stake of Proof와 같은 널리 알려진 알고리즘과 어떻게 다릅니까?

PoS 및 PoW는 채굴을 사용합니다. 채굴자들은모든 블록에 대해 새로운 코인을 블록 보상으로 받습니다.
따라서 채굴자들은 돈을 벌고 있으며 네트워크를 통제하기 위해 노력할 것입니다. 
새로 생성된 코인이 인플레이션을 일으키기 때문에 모두가 고통을 겪습니다. 
스카이코인은 채굴을 제거하고 인플레이션을 없애기 위해 만들어졌습니다. 
블록 보상, 새로운 코인이 없습니다. 그리고 우리는 이를 수행하기 위해 새로운 합의 알고리즘을 개발할 필요가 있었으며,
이러한 제약을 만족하는 방법은 몇가지 밖에 없었습니다. 
이 조건을 만족하기 위해서, 이 합의 알고리즘은 분산시스템 상에서 합의 달성을 위한 Ben-Or의 무작위 추출 절차에 기반하며, 
합의 프로세스를 중단시키려는 적대적 또는 악의적 노드를 방어하는 능력을 향상시켜줍니다.
이것은 skycoin.net의 화이트백서에 자세히 기술되어있습니다. 
나는 그것을 "네트워크 합의"라고 부르며, 그것은 일종의 신뢰의 웹(WoT)을 사용합니다.
블록을 만드는 사람들이 나쁜 일을 벌이거나 네트워크를 공격한다면 커뮤니티는 이를 제거할 수 있습니다. 
동시에 네트워크를 제어하는 사람들은 트랜젝션 속도를 늦추거나, 성가신 일을 처리하는 것을 제외하고는 네트워크를 실제로 공격할 권한을 
가지고 있지 않습니다.
따라서 그들이 악성사용자가 된다면, 단지 어떻게 그들을 내쫓고 새로운 사람들을 선출할 것인지 고민하는 것만이 문제가 됩니다.   


**mike**
언제 스카이와이어를 출시하고 하드웨어 노드(testnet 또는 mainnet)에서 테스트 할 것인지에 대해 계획이 있습니까?(테스트넷 또는 메인넷)

**mgaruccio**
그렇다면 만약 블록 보상이 없다면 노드를 운영하는 인센티브는 무엇입니까?

**vega**
스카이코인(코인 자체)의 실제 기능은 무엇입니까? 코인은 화폐로 쓰일 것이며, 
이 모든 다양한 개발 기능들 간 가치가 전가되거나, 모든 것을 합치는 반-개별 프로젝트가 되거나, 또는 뭔가 기능이 제한 되는 것인가요?

**michaelthecryptoguy**
노드의 사양에 대한 생각이 있습니까? 처음에는요? 10,000명의 사용자에 대해 어떻게 생각하십니까?(편집됨)

**synth**

> 제 생각에는 nex가 괜찮다고 생각해요.

3명이 코인의 30%를 각각 소유했습니다. 한명은 나가기를 결심하고 덤핑을 시작했습니다. 제가 알고 있기로는 NXT는 1억 5천이(150 million) 넘었습니다.
그가 덤핑을 시작했을 때, 이미 NXT는 끝났습니다.
스카이코인의 배포는 설립자와 초기 투자자들의 덤핑을 막기 위해 고안되었습니다.
스카이코인이 분배된 전체 코인의 30 %를 얻은 후, 풀리지 않은 나머지 코인을 얻기는 힘들 것이며, 매년 잔여 코인의 최대 5%가 출시될 수 있습니다.
따라서 코인의 나머지 70 %에 대한 분배는 최소14 년이 소요됩니다.(더 길 수도 있습니다.)
우리는 코인의 보유분을 팔 수 없습니다. 우리가 코인 당 5 달러로 10 %를 팔면 5,000만 달러가 될 것인데, 
우리는 이것을 쓰거나 전액을 사용할 수 없습니다. 아직 이 단계가 아닙니다.
이더리움은 ICO 이후 1, 2년 동안 3천만 또는 7천만 달러를 소비한 다음 거의 파산했습니다. 
실리콘 밸리의 임금 및 사무실 등, 우리는 매우 절약하고 있으며, 그것에 대해 책임감을 가지고 있습니다.
이제 우리는 EOS와 같은 동전을 가지고 있으며, 그들은 10억 달러를 모으고 싶어하지만 아직 아무 것도 생산하지 않았고, 
블록 체인을 소유하지 않았으며, 그 돈을 어떻게 쓸지 모르지만, 
마케팅을 위해 시간 당 35만 달러를 소비하고 있습니다./ 홍보 등 ...

**arc-over-water**
무엇이 당신이 판매를 하지 못하게 합니까? 누구나 수익금을 쓸 수 있습니까? nxt는 sky보다 나중에 나온 새로운 플랫폼이며, 
시장 가치는 2억 2천만 달러와 1억6천 6백만 달러입니다. 
나는 당신이 말하는 것을 들었지만, 증거는 다릅니다.
Nxt의 커뮤니티는 거대하며 활동적입니다. 하지만 당신이 망했다고 말했는데, 내가 그걸 알아내지 못합니까?

**synth**

> 스카이코인(코인 자체)의 실제 기능은 무엇입니까? 코인은 화폐로 쓰일 것이며, 
이 모든 다양한 개발 기능들 간 가치가 전가되거나, 모든 것을 합치는 반-개별 프로젝트가 되거나, 또는 뭔가 기능이 제한 되는 것인가요?

네, 비트코인은 아무런 목적이 없습니다. altcoin은 두 가지 기능을 합니다 - 당신의 잔액을 확인하고 - 다른 사람들에게 돈을 보내줍니다. 
두 가지 기능 - 잔액 확인 - 보내기
코인에 가치를 부여하기 위해서는, 사람들이 특정 서비스를 사용하기 위해 그것을 구매해야 합니다.
사람들이 코인을 쓸 재화가 있어야하며, 거기에는 수요가 있어야합니다. 
따라서 비트코인은 실제로 순전히 투기 자산입니다. 
현금 흐름을 발생시키지 않으며 그 가치는 인식 또는 사회적 상황에 따라 결정됩니다. 
이상적으로, 스카이코인은 "더 나은 비트코인"(더 빠르고, 더 안전하고, 새로운 알고리즘, 단순함 등)으로 출발할 것이고, 
시간이 지남에 따라 우리는 생태계를 구축하고, 몇 가지 종류의 투자를하고 네트워크와 사용자 기반으로 코인의 가치를 고정시킬 것입니다.
메쉬 네트워크(스카이와이어)는 사람들이 코인을 얻기 위해 무엇인가를 주고, 사람들이 동전을 소비할 수 있기 때문에 좋은 것입니다.
당신은 스카이와이어를 통해 터널링하는 VPN을 통해 당신의 인터넷 트래픽을 실행할 수 있으며,  
아마도 명목상의 금액(사실은 엄청나게 적은 금액)이지만, 실제 경제 활동과 실제 사용자 기반 및 커뮤니티가 코인을 사용해서 이루어 질 것입니다.
단지 투자가 아닙니다. 나중에 범위가 훨씬 넓어집니다.

**arc-over-water**
그래서 스카이코인 지갑은 인터넷 사용을 위한 VPN이 될 것입니까?

**synth**

> nxt는 sky보다 나중에 나온 새로운 플랫폼이며, 시장 가치는 2억 2천만 달러와 1억6천 6백만 달러입니다. 
나는 당신이 말하는 것을 들었지만, 증거는 다릅니다.
Nxt의 커뮤니티는 거대하며 활동적입니다. 하지만 당신이 망했다고 말했는데, 내가 그걸 알아내지 못합니까?

제가 말한 것은 NXT가 이더리움과 현재보다 많은 발전가능성이 있을 것이라는 것입니다. 배포와 과다 집중 문제를 제외하고 말입니다.
그것은 몇 년전으로 그것을 되돌려 놓았습니다.
초기 고래들 중 하나가 매각을 시작하거나 그것을 고려할 때, 장기적으로 그것이 가격에 어떤 영향이 있을 지를 전혀 고려하지 않았습니다.

**arc-over-water**
그러나 IOTA의 리드개발자도 똑같은 행동을 했고... 그들이 배포한 시장 가격은 100만 달러를 넘습니다.

**synth**

> 그래서 스카이코인 지갑은 인터넷 사용을 위한 VPN이 될 것입니까?

VPN은 단순 어플리케이션으로, 스카이와이어의 대역폭을 사용합니다.
개발에는 몇 가지 사항이 있습니다. CXO와 함께 완전히 배포된 4chan와 같은 BBS입니다. https://github.com/skycoin/bbs Skywire
이것 또한 스카이와이어를 통해 실행됩니다. 이것은 처음부터 완전히 새로운 인터넷을 구축하는 것과 같습니다. 
GitHub skycoin / bbs GitHub에 계정을 만들어 bbs 개발을 하고 있습니다.

**mike**
그래서 스카이코인은 리소스 기반 코인이며, 이것의 가치는 유용한 서비스의 제공에 의해 뒷받침되며, 이것은 개인적이며 안전한 네트워킹이라는 것입니까?
분산 스토리지와 분산 포로세싱을 추가할 계획이 있습니까?

**arc-over-water**
그래서 100개의 개별적인 계정에 100만 개의 코인이 있는 100 ICO가 될 것입니까? 배포 패턴은 어떻게 됩니까?
그것은 코드 또는 개발현황에 기록됩니까?

**rockyj**
!계산해주세요.

**slackbot Custom Response**
https://docs.google.com/spreadsheets/d/1FGo3FkC3uSWXGHatPQyny2brMWjAIJsHFCR-Lhkl_m0/edit#gid=0

**synth**

> 그렇다면 만약 블록 보상이 없다면 노드를 운영하는 인센티브는 무엇입니까?

합의 노드를 운영하는 것은 비용이 들지 않습니다. 
당신은 라즈베리 파이로 그것을 운영할 수 있습니다.
다른 중요한 것은, 합의를 하는 사람들이 나쁜 행동을 하는 경우, 커뮤니티가 그들을 제거하고 대체할 수 있다는 것입니다. 
또 다른 중요한 점은, 그들이 프로토콜을 준수하고 있는지를 자동으로 감사하고 결정할 수 있다는 것입니다.
스카이코인의 채굴자는 강력한 권한을 행사할 수 없으며 트랜젝션의 속도저하를 제외하고는 아무 것도 할 수 없습니다.
그들은 개인키 없이 다른 사람들의 돈을 쓸 수 없으므로 합의/채굴 노드는 거의 무의미 합니다. 
채굴자들이 네트워크 인질을 붙잡거나 이기적으로 행동 할 수 있는 비트 코인과는 다릅니다.
(개인 이익을 위해 거래 수수료를 높이고 모든 사람을 위한 비트 코인 발전을 지연시키는 등)

> 그래서 스카이코인은 리소스 기반 코인이며, 이것의 가치는 유용한 서비스의 제공에 의해 뒷받침되며, 이것은 개인적이며 안전한 네트워킹이라는 
것입니까? 분산 스토리지와 분산 포로세싱을 추가할 계획이 있습니까?

우리는 CXO라고 불리는 분산 스토리지를 가지고 있습니다. 그러나 단지 대역폭은 스카이와이어에 의한 수익만을 창출합니다. 
우리는 모든 API 호출에 코인 비용을 부과하지 않고 한 푼도 지불하지 않습니다.
무료가되어야 하는 모든 것은 무료입니다. 그래서 그것은 다른 철학을 가지고 있습니다. 
CXO는 소셜 미디어 애플리케이션(Steemit과 유사함)을 배포했습니다. 
CXO는 IFPS와 매우 유사하지만 내부 인프라 및 암호 표준을 사용하여 간단하게 설계되었습니다.

**mike**
스카이코인은 네트워트 상의 피해로 인한 악성 노드 또는 지연 노드 상에서 최적의 경로와 라우트를 선택하는 것이 가능합니까? 
합의알고리즘 상에서 이것의 피해를 줄이는 것이 가능합니까?
내가 타이핑하는 동안 위의 질문에 답한 것처럼 보이네요...

**tranzer**
스카이코인은 얼마나 많은 tx/s를 처리할 수 있습니까? 블록 시간이란 무엇입니까??

**thrice.pi**
300 맞죠? ^

**arc-over-water**
당신의 웹사이트에서는 당신이 Non-Turing 완전언어를 사용할 것이라고 써 있습니까? 

**synth**

>그래서 100개의 개별적인 계정에 100만 개의 코인이 있는 100 ICO가 될 것입니까? 배포 패턴은 어떻게 됩니까?
그것은 코드 또는 개발현황에 기록됩니까?

곧 웹 사이트에 배포 페이지가 생길 것입니다. 이것은 복잡한 문제입니다.
스카이와이어는 네트워크 활동에 대한 일종의 십일조를 통해 코인을 순환에서 벗어나게 하기 위해 개발되었으며, 
이것은 자동으로 배포를 효과적으로 조절합니다.
따라서 배포는 실제로 정점에 도달한 후 감소합니다.
그러나 하나의 배포은 잠긴 코인에서 이루어지며, 잠긴 코인은 풀린 후 순환하고 소멸됩니다.(스카이와이어의 십일조는 순환에서 제외됩니다.) 
그러나 여전히 많은 양의 코인이 네트워크에 있습니다.
코인 보유자에게는 코인하워(coinhour)라는 배당금이 지급되며, 코인하워(coinhour)와 스카이코인 사이에 시장 환율이 변환될 것이고,
코인하워(coinhour)는 스카이와이어 네트워크의 실제 통화입니다. 
코인하워(coinhour)가 충분하지 않으면 코인하워(coinhour)를 위해 스카이코인을 시장 가격으로 팔아 대역폭을 구입하십시오;
하지만 코인이 많다면 영화나 VPN 등을 다운로드 할 수 있는 충분한 코인하워(coinhour)를 가질 수 있으며 이것은 본질적으로 무료입니다. 
따라서 이중 수준의 경제 구조가 있습니다. 둘 다 코인을 매매하면서 코인을 매도하고 사용자가 네트워크를 사용하는 경우
코인을 매수하도록 유도하는 배당금이나 인센티브를 제공합니다.

**arc-over-water**
그래서 2가지 종류의 통화가 있고, 하나는 보유하고 다른 하나는 소비하네요.

**synth**

> 스카이코인은 네트워트 상의 피해로 인한 악성 노드 또는 지연 노드 상에서 최적의 경로와 라우트를 선택하는 것이 가능합니까? 

네, 이것은 매우 중요합니다.
연결을 시도하는 사람은, 연결 경로를 선택합니다!
당신은 비디오 게임이나 스카이프를 위해 최소 대기경로를 선택할 수 있으며, 비디오 다운로드 등을 위해 최고 처리 경로를 선택할 수 있습니다.
또는 특정 노드나 시설 또는 국가 경로를 선택할 수 있습니다. 트래픽이 탈취될 수 있는 보안 문제와 트래픽이 발생할 수 있는 지점 수를 
최소화 할 수 있습니다.

**mike**
스카이코인은 원래 계획대로 메쉬 노드를 설정하고 등록하기 위한 노드 보조금 계획을 여전히 갖고 있습니까?

**dr10**
언제 대중에게 계획된 기술과 서비스를 제공할 계획입니까? 그들이 당신들이 성취한 것을 언제 사용할 수 있습니까?

**synth**

> 당신의 웹사이트에서는 당신이 Non-Turing 완전언어를 사용할 것이라고 써 있습니까? 

이것은 아마 오류일 것입니다. LOL. 우리는 곧 새로운 웹 사이트를 갖게 될 것입니다.
스카이코인 블록체인은 스크립팅 언어가 없습니다.
각 거래는 일정한 시간(효율성과 보안 및 가장 높은 거래률을 달성하고 코인을 간단하게 유지하기 위해)에 이루어집니다.
그러나 우리는 CX라는 개발 언어를 사용합니다.이 언어는 "스마트 계약"을 넘어서는 차세대 언어이며 이더리움 상의 장난감입니다.
그것은 변조 불가능한 데이터 구조를 사용하며 완전히 새로운 것입니다. 
스카이코인"스마트계약"의 대부분은 블록 체인 밖에서 실행되거나 개인 블록체인에서 실행될 것입니다. 
우리는 모든 데이터를 메인 체인에 유지하고 싶지 않고, 왜냐하면 모든 사람이 모든 데이터를 다운로드하도록 강요한다면 그것은 단지 스팸이고
블록체인은 죽을 것이기 때문입니다. 더 좋은 방법이 있습니다.

> 스카이코인은 원래 계획대로 메쉬 노드를 설정하고 등록하기 위한 노드 보조금 계획을 여전히 갖고 있습니까?

네, 우리는 스카이와이어 노드, 합의노드 및 서비스를 실행하는 사람들을 위해 네트워크 인센티브를 코인의 20%에서 30%까지 분배할 것입니다. 
나는 이것이 엄청난 마케팅이 될 것이라고 생각합니다. 모든 코인을 고래가 가지고 있는 대신 사용자에게로 가지고 오는 것이 가장 좋은 방법입니다.

**samuelvihollandia**
나는 스카이코인이 VPN 연결에 사용될 수 있다고 당신이 제안한 것을 읽었습니다. 이것이 당신이 알고 있는 가장 큰 활용 사례입니까?

**arc-over-water**
Maidsafe는 약 10 년 동안 넷의 재설계를 위해 노력해 왔는데, 그들이 하고 있는 것과 어떤 것이 똑같고 어떤 것이 다릅니까?

**synth**

> 나는 스카이코인이 VPN 연결에 사용될 수 있다고 당신이 제안한 것을 읽었습니다. 이것이 당신이 알고 있는 가장 큰 활용 사례입니까?

아니오. 그것은 단지 우리가 일하고 있는 것 중 가장 쉬운 부분입니다. 그것은 가장 큰 어플리케이션이 아닙니다.
현재 인터넷 트래픽의 80 %는 비트토렌토(bitorrent)가 점유하고 있으며, 비트토렌토(bitorrent) 사이트는 체계적으로 폐쇄되어 인터넷에서 
사라질 것입니다. 그들은 완전히 떠나지 않을 것이지만, 바닥에 떨어질 것입니다. What.cd(최대 규모의 음악 사이트, 약 800k 명)가 막 폐쇠되었으며, 
bakabt (최대 애니메이션 사이트)는 등록이 종료되었고, Nyantorrent 등...
수백만 명의 사용자 커뮤니티가 Clearnet(기존 기업의 쓰레기-망)을 "새 인터넷"으로 변경합니다. 
우리는 수많은 사람들이 수백만 명의 전체 사용자 커뮤니티로 이동하는 것을 보게 될 것입니다.

**arc-over-water**
당신은 법인입니까 아니면 재단입니까 아니면 자선 단체입니까? 등록? 나는 아무것도 확신하지 못합니다. 당신은 누구입니까? 
개발(dev) 팀의 크기는 얼마입니까? 배경? - Maesafe는 개방적이고 명확하므로 IOTA와 Stellar 등이 있습니다. 
당신과 당신의 팀이 누구인지 알려줄 수 있습니까? 특히 당신은 15년 이상의 미래에 대해 이야기하고 있습니다.

**techbytes**
우리가 스카이와이어 노드를 실행하려면 스카이코인, 다른 동전의 마스터노드와 같은 합의 노드가 필요합니까?

**synth**

> Maidsafe는 약 10 년 동안 넷의 재설계를 위해 노력해 왔는데, 그들이 하고 있는 것과 어떤 것이 똑같고 어떤 것이 다릅니까?

Maidsafe는 버전2 또는 3입니다. Maidsafe는 버전 9까지 실제 코인을 가지지 않습니다. 
각 버전에는 약 2 ~ 3 년이 소요됩니다. Maidsafe는이 비율로 적어도 18 년 동안 "완료"되거나 준비되지 않습니다. 
스카이코인은 ~ 6 년 동안 개발 중이며 4 년 동안 메쉬넷을 구축했으며 몇 달 후에 완성 될 것입니다. 
사람들은 그것을 사용할 수 있습니다.
스카이코인은 목적에 있어서 maidsafe와 비슷하지만, 접근 방식과 설계 및 근본이 다릅니다. 
우리는 모든 일을 하려고 하지는 않았지만, 작고 다루기 쉬운 핵심에 초점을 맞추었습니다. 
이 분야에는 여러 개의 프로젝트가 존재하지만, 단지 몇몇 팀만이 정해진 시간 안에 새로운 인터넷을 구축하거나 시스템의 각 구성 요소 설계를 
계획할 수 있으며, 또는 이 거대한 시스템의 각 기능을 디자인 할 수 있고, 10년이 걸릴 수도 있는 이 프로젝트의 각 단계별 구성을 어떻게 
효율적으로 실행할 것인지를 알아낼 수 있습니다.(편집됨)

**mike**
Ark와 스카이코인이 시너지 효과를 발휘할 수있는 방법을 볼 수 있습니까? 나는 바퀴를 위해 투자하지 않을 것이며, 
특히 이것은 스카이코인 같은 것으로 대체되는 것으로 보입니다.  
Skycoin이 본질적으로 TCP/IP를 대체하고 하드웨어 레벨에서 메쉬 네트워크 유형의 기능을 제공하는 것을 보았을 때, 
Ark는 최상위 애플리케이션 레이어로서 작동할 것입니다.

**arc-over-water**
Maidsafe에 대한 최신 정보를 제공합니다. 그들은 Alpha에서 거의 벗어났으며 내년 초에 출시될 예정입니다. 
하지만 Maidsafe는 그것이 출시되면 바이러스나 인공 지능(AI) 유형과 마찬가지로 타우 체인(Tau Chain)과 헌터 
마이너 크라프터(HunterMinerCrafter)의 오토 노믹 (Autonomic)도 AI를 지향하고 있다고 하는데, 
스카이 타우(Sky Tau) 및 오토 노믹 (Autonomic)은? 

**dr10**
스마트 브리지가 왔다! : 카파 :

**mike**
그래서 스카이코인은 세계적인 글로벌 분산 클라우드 서버를 구축하기 위해서 동작합니다.
통신하기 위해서, 특정 서버에서 메시지 또는 호스팅 사이트를 보내는 것보다는 선택한 수신자에게 암호화된 파일을 공유하는 것이 좋습니다. 

**synth**

> 당신은 법인입니까 아니면 재단입니까 아니면 자선 단체입니까? 등록? 나는 아무것도 확신하지 못합니다. 당신은 누구입니까? 
개발(dev) 팀의 크기는 얼마입니까? 배경?
제가 알기로는 스카이코인을 위해 일하거나 큰 기여를 하고 있는 사람들이 60명이 넘습니다. 이것은 본질적으로 darknet으로부터 시작된 프로젝트입니다.
많은 기여자들은 익명으로 활동합니다. 그들 중 일부는 군용 산업단지에 있어서 보안 제약사항이 있으며, 그중 한 명은 샌디에고 해군 방위 연구소에서 근무하고 있습니다. 그 곳에서 자금 지원을 받아 네트워크 프로토콜에 대한 많은 아이디어가 공공연구기관에서 나왔습니다.
우리는 또한 비트코인 초창기 개발자들이 있으며, 비트코인 핵심 개발자 이전의 하드코어 개발자들을 많이 보유하고 있습니다. 
중국 쪽에는 알리바바 및 통신 초기 투자자들이 있습니다. 그리고 중국 항공 그룹(4개의 민영 항공 회사 소유)과 시노펙(Sinopec)
(현재 세계2위 상장법인)과 조종사들이 있습니다.
다음으로 우리는 이스라엘과 미국의 정보 기관 요원이 있으며, 아마도 그들은 돈 세탁 또는 심리전을 하고 있을 것입니다. 
그들은 어떤 이유에서인지 금방 드러났습니다. 이 그룹들은 이 코인의 "어플리케이션"과 트랜젝션 정보보호 향상방법 및 CoinJoin 프로토콜의 세부사항에 
대해 매우 관심이 있는 것으로 보입니다. 우리는 법의학 회계에 경험이 풍부한 사람들로부터 많은 조언을 받았고, 그들이 무엇을 알고 싶어하는지 
그리고 그들이 비트코인에 대해 부족한 점과 메타데이터가 어디에서 유출되었다고 생각하는 지에 대해 알아냈습니다. 
다음으로 각 분야의 박사 급의 사람들은 분산형 데이터베이스 합의 알고리즘을 연구하고 있으며, 또 다른 그룹은 프로그래밍 언어를 연구 중입니다.
다음으로 많은 사람들이 deep darknet, anon, frog twitter 그리고 chpher punks 그리고 비트토렌트(bitorrent) 커뮤니티에 있습니다.
(실제로는 2개의 분리된 그룹으로 구성) 그리고 러시아 darknet 커뮤니티의 사람들이 있습니다. 우리는 8명의 Ivan이 있습니다.(편집됨)
> 제가 보기에 스카이코인은 본질적으로 TCP/IP를 대체하고 하드웨어 레벨에서 메쉬 네트워크 유형 기능을 제공하며, Ark는 최상위 애플리케이션 
레이어로 작동합니다.

네, 그 키는 2가지 기능으로 작동합니다. - 공개키로 사람들에게 연결하는 것(네트워킹) - 자체검증 분배, P2P(peer to peer)를 활용한 데이터 변조불가
(트랜젝션, 블록 등...컨텐츠 주소지정이 가능한 저장소)
그리고 당신은 두 빌딩 블록에서 거의 모든 것을 구축할 수 있습니다. 전체 인터넷은 궁극적으로 원본 위에 다시 쓰여질 것이고 많은 기존 프로토콜을 
대신할 것입니다.

**arc-over-water**
자금을 지원하는 단체는 누구입니까? 나는 당신이 2개의 ICO를 끝냈다고 생각합니다. 얼마를 받았습니까? 첫 번째는 10c이고 두 번째는 동전 당 @50c이고, 6백만 개가 출시되었습니다. 맞습니까?

**samuelvihollandia**
곧 다른 거래소에 상장할 생각이 있습니까?

**arc-over-water**
당신은 스카이코인이 시작할 때 개인적으로 보유하고 있는 것이 있습니까? 회원은 무엇을 가지고 있습니까?
누가 ICO 자금 등을 분배하나요... 나는 당신이 투자의 분권화가 양날의 검인 것을 이해하기를 바랍니다. 
우리는 사람들에게 투자하지만 이 사람들이 누구인지 알 수가 없습니다 .... 그래서 ... 우리는 질문합니다..(편집됨)

**thrice.pi**
스카이코인을 구축하는데 도움을 주는 모든 외부 인원들과 함께하며, 현재 이들은 주요 핵심 팀과 함께하며 멋진 기능들을 계속 진행하는데 큰 도움을 
주고 있습니다. 이러한 외부 인원을 장기간에 걸쳐 모집할 것입니까?

**synth**

> 자금을 지원하는 단체는 누구입니까? 나는 당신이 2개의 ICO를 끝냈다고 생각합니다. 얼마를 받았습니까? 첫 번째는 10c이고 두 번째는 동전 당 @50c
이고, 6백만 개가 출시되었습니다. 맞습니까?

처음 4년 동안 이 프로젝트에 자금을 지원한 사람들은 초창기 비트 코인(bitcoin)과 딥 크립토(deep crypto) 사람들 ; 
비트 코인(Bitcoin)과 다른 알트(alts)가 핵심 이슈에 전혀 관심을 보이지 않는다는 사실에 불만을 가진 사람들 이었습니다.
제가 알기로, 그들은 몇 년에 걸쳐 1200 비트코인 이상을 우리에게 제공하였고, 그 댓가로 아무것도 요구하지 않았습니다.
초기 스카이코인 개발자는 학술 연구, 아키텍처 및 새로운 알고리즘을 수행하고 있었습니다. 프로토 타이핑 및 시뮬레이션 등. 
이후 단계의 사람들은 더 많은 프로젝트 관리와 구현을 수행했습니다.
우리는 적은 금액으로 4개의 ICO를 수행했고, 프로젝트 개발에 참여한 개발자가 구매할 수 있도록 했습니다.
기억하는 첫 번째 ICO는 코인 당 0.10 달러였습니다. 가격은 이제 코인 당 약 $ 4.00이므로 최대 35배 ~ 40배입니다.
그러나 비트코인 가격이 $100에서 $3000으로 상승한 것을 고려할 때, 그 상승폭은 그리 크지 않습니다. lol (편집됨)

**arc-over-water**
그 가격이 약 1년 만에 35배가 되었는데, 이제 가격을 동결시키고 다른 ICO를 출시할 때가 아닐까요? 얼마만큼의 코인을 출시하고 어떤 절차를 밟습니까?

**mike**
인텔 Edison이나 Joule, 또는 삼성 Artik 10이 스카이와이어 무선 노드로 잘 작동할까요? 그것들은 2Gb-8Gb RAM, 8-64Gg eMMC 저장 장치, 
802.11n 무선, 블루투스 및 일부 Zigbee가 있습니까?

**synth**

>당신은 스카이코인이 시작할 때 개인적으로 보유하고 있는 것이 있습니까? 회원은 무엇을 가지고 있습니까?
누가 ICO 자금 등을 분배하나요... 나는 당신이 투자의 분권화가 양날의 검인 것을 이해하기를 바랍니다. 
우리는 사람들에게 투자하지만 이 사람들이 누구인지 알 수가 없습니다 .... 그래서 ... 우리는 질문합니다..(편집됨)

제가 알기로는, 처음 3년 동안 지금은 합병된 세 개의 다른 그룹이 비슷한 목표를 가지고 있었다고 생각합니다. 
코드가 다른 언어로 작성 되었기 때문입니다. 파이썬, C 코드가 있었고 결국에는 golang이 되었으며, 현재 golang 코드가 현재 코드베이스의 기초가 
되었습니다.
코인 할당이 작동하는 방식은 코인을 공개하는 것에 대한 익명의 동의가 필요하며, 특정한 목적이 있어야 하며, 모든 개발자가 이를 차단할 수 있습니다.
다음으로 다양한 프로젝트 관리자에게 할당하기 위한 비트코인들이 있습니다. 그리고 그것은 개발자, 계약자, 마케팅 등을 위한 운영 자금입니다. 
그리고 다른 사람들은 각자 다른 책임들이 있습니다.
다음으로 우리는 또한 자금지원 및 후원을 받는 회사가 있으며, 일부 회사는 풀 타임 개발자에게 임금을 지불하는 등 많은 도움을 줍니다.

**arc-over-water**
실리콘 밸리(TV 쇼)는 최근 네트워크나 냉장고에서 그들의 분산 웹을 운영하고 있습니까? 그래서 제가 생각하기로는, 스마트폰, 스마트 기기?
가정용 기기 등이 서비스를 추가하고 Sky로부터 보상을 받을 수 있습니까?

**mike**
가장 좋은 방법은 노드의 백도어를 막기 위해 완전한 오픈소스와 공개적으로 감사된 제작시스템이 칩으로 제작되는 것입니다. 
이제는 칩 설계자들도 ASIC 디자인에 IP 코어로 알려진 블랙 박스를 드래그 앤 드롭하기 때문에 칩에 무엇을 넣고 있는지 알지 못합니다.

**synth**

>그 가격이 약 1년 만에 35배가 되었는데, 이제 가격을 동결시키고 다른 ICO를 출시할 때가 아닐까요? 얼마만큼의 코인을 출시하고 어떤 절차를 밟습니까?

제가 알기로는, Skycoin 가격이 40일마다 두 배가 되고 있습니다. 그러나 여전히 상위 20위 안에 들기까지 몇 년이 걸릴 것입니다. 
6년 동안 하루 1% 씩 성장 했음에도 불구하고 비트코인이 0에서 1 달러로 떨어지는 것을 보았습니다.

> 가장 좋은 방법은 노드의 백도어를 막기 위해 완전한 오픈소스와 공개적으로 감사된 제작시스템이 칩으로 제작되는 것입니다. 

우리는 arm을 사용하려고 합니다.

**arc-over-water**
IOTA는 노드를 위해 자체 하드웨어를 제작하고 있습니다. 3대 자산은 JINN입니다.

**synth**
모든 intel 및 AMD 시스템에는 원격 관리 엔진 백도어가 있습니다. 그래서 그들은 많은 양의 코인을 보관하는데 안전하지 않습니다. 
우리는 알파인 리눅스와 6MB 사양에 우리의 툴 체인에서 구동하기 위한 사양을 갖춘 리눅스 특별버전을 가지고 있습니다. 
커널에 바이너리 blob들이 없거나 소스에서 컴파일 할 수 없는 것이 있습니다. 
systemd가없고 gli가 없지만 musl을 사용합니다. 그리고 openssl을 가지고 있지 않습니다.

**mike**
그리고 Samsung Artik 5와 10 같은 기기에서 아무런 문제없이 실행할 수 있습니다. 그것들은 ARM 기반입니다. 
Artik 10을 위한 25x35x4mm 패키지인 Artik 5는 작고 강력하지만, 2 개의 별도 안테나 포트가 있어 옴니 안테나와 지향성 안테나가 있는 메시 
네트워킹에 좋습니다.

**earlyarkinvestor**
Ark는 Lisk와 비교했을 때 어떻습니까?

**synth**
업로드 이미지: 1923810435.jpg 설명 추가

**earlyarkinvestor**
Lisk는 블록체인 간의 상호 운용성을 달성하려고 시도하지 않습니다.

**synth**
업로드 이미지: 1433594905.jpg 설명 추가

**synth**
업로드 이미지: 1432540863.jpg 설명 추가

**synth**
업로드 이미지: 2049465686.jpg 설명 추가

**mike**
멋지군요! ARM 기반 서버 랙 같군요.
도움이 필요하면 알려주세요. 당신의 solidwork을 확인하겠습니다. 나는 그것을 아주 잘 합니다.

**synth**
이것은 스카이코인 클러스터입니다.; 8개의 CPU 보드가 있으며 ; CPU 당 4 코어, CPU 당 2GB RAM 및 64비트 ARM 프로세서가 있습니다.
단지 하나의 프로그램만 각 개별 보드에서 실행되므로, 따라서 시스템 상 손상된 1개 프로세스가 시스템 상에 구성된 모든 프로세스에 접근하여 영향을
줄 수 없도록 구획화와 물리적 갭이 있는 것입니다.

**mike**
보드 당 2 개의 이더넷 포트가 있는 것처럼 보입니다.

**synth**
그리고 하드웨어는 퀄컴 백도어를 가지고 있지 않으며 그것은 실제로 중국 장비입니다.; 그리고 백도어는 일반적으로 커널 수준이며 그들은 아직 하드웨어
수준 백도어를 구현할 수 없기 때문입니다. lol

**mike**
그것은 SATA 포트가 있습니까, M.2 스토리지 입니까?

**synth**
그리고 우리는 결국 ARM 개방형 라우터를 갖게 될 것입니다. 이 모델은 SATA가 없지만; SATA가 있는 모델이 있습니다.; 
당신은 16개의 2TB 드라이브를 연결하고, lol 그리고 piratebay를 당신의 클러스터에 다운로드 합니다.(편집됨)
스카이코인 인프라구성은 클러스터 기반이며 300대 이상의 컴퓨터에서 실행되도록 설계되었고, 컴퓨터 당 하나의 "노드"가 배치됩니다. 
CXO 스토리지 노드 또는 스카이와이어 SDN/메쉬넷 노드 또는 VPN 엔드 포인트 노드 또는 합의 네트워크 또는 스카이코인 노드 등을 사용합니다. 
우리는 다양한 노드/응용 프로그램 유형이 있습니다. 그래서 이것은 "개인 클라우드"그 자체로 StoreJ와는 다른 것입니다.; 
당신은 ~ 5 클러스터 및 300 대의 컴퓨터를 사용할 수 있으며, 당신의 파일을, 당신의 인터넷에, 당신의 하드웨어에 저장할 수 있습니다. 
당신은 당신의 자체 네트워크 외부로 이동할 필요가 없습니다.

**mike**
모든 케이블이 없는 SSD 어레이를 실행하기 위한 M.2 소켓 배열을 가진 보드를 가지고 회로 보드에서 버스를 차폐하는 것이 좋을 것 이라는 생각이 드네요.

**synth**
네, 결국 m.2가 될 것입니다. 실제로 저장용 microSSD를 사용할 것입니다. 48MB/s와 함께요.

**mike**
수량에 따른 ARM 보드 가격 책정에 대한 아이디어가 있습니까? 우리는 Bitseed V3용 인텔을 보고 있지만, ARM이 있으면 좋을 것입니다. 특히 SATA가 있는 보드를 사용하는 것이 좋습니다.

**arc-over-water**
다음에 출시될 수있는 유용한 기능에 대한 일반적인 아이디어가 있습니까? 첫번째 발표는 코인과 지갑이었고, 다음 ICO와 일반적인 향후 일정이 있습니까?

**synth**
보드는 각각 30 달러이고 솔리드 스테이트를 위한 메모리는 실제로 CPU/RAM/보드 비용보다 훨씬 높습니다. 이것은 일종의 모험입니다.

**mike**
그리고 당신은 microSSD를 가지고 있는데, 최대크기는 얼마입니까? 우리는 지금 즉시 1개의 Tb 하드 드라이브와 함께 배송할 것입니다.

**synth**
Bitseed 마이크가 이것을 도와줄 것입니다.; 그래서 우리는 보드를 풀링하고 커스텀 PCB를 할 수 있습니다.

**mike**
네, 우리는 RAM과 eMMC에서 가격상승을 생각하고 있습니다. 그리고 저렴한 SATA 보드를 찾기가 어렵습니다.

**synth**
orange pi를 사용해보십시오. 가격은 SATA의 경우 30% 상승합니다.

**mike**
네, 아주 좋은 사양입니다.

**synth**
사실은, 우리는 커스텀 PCB를 제작할 것이며 그리고 그것은 플러그 가능한 블레이드 서버라고 생각합니다.

**mike**
마이크 저는 드론 라우터, cubesat/picosat 사용을 위한 소형 폼 팩터로 삼성 Artiks를 좋아합니다. 
그러나 그 사실은 당신이 당신의 보드의 공급체인의 깊은 곳에서 통제한다는 것이죠.

**synth**
우리는 단지 램, CPU, microSD 슬롯만 필요로 합니다.; 그리고 그것이 바로 이것입니다. 그래서 wifi와 모든 다른 것들은 단지 쓰레기입니다.
우리는 통신, 저장 및 계산만 할 수 있습니다. 그래서 최소화로 가야 합니다.

**mike**
네, 우리는 pcduino nano 포트를 거의 사용하지 않으며, 비디오,오디오,IR는 필요하지 않습니다.

**synth**
그것은 오픈 소스 FPGA 툴체인과 서브트랙과 JNZ(jump if not zero)기능을 가진 1개의 명령 컴퓨터로 구성되어 있습니다.; 그리고
당신이 램과 바이트 배열이 있그것을 컴파일할 수 도 있습니다.; 그것은 트롤링이지만, 트랜젝션 서명과 다른 것을 위하서, 당신이 운영할 수 있는
수준에서 운영할 수 있습니다.

**mike**
FPGA에 대한 링크가 있습니까? 내가 가장 좋아하는 제품은 ZYNQ 7000 시리즈이지만, 이것의 가격은 훨씬 저렴합니다.

**synth**
저는 FPGA에 대해서 물어봐야 합니다.

**mike**
Blue Canyon은 큐브 위성 버스를 위해 ZYNQ 7000을 사용합니다.

**synth**
그것은 상하이에 있는 연구 회사입니다.

**thrice.pi**
나는 당신과 마이크의 대화가 혼란스러워지는 것을 원치 않습니다. 마이크는 2가지 질문을 했는데 그것에 대해 계속 진행해주세요.
그러나 나는 아직 마이크가 이전에 한 간단한 질문에 대한 답을 보지 못했습니다. 그는 스카이코인 노드를 돌리기 위해 필요한 사양이 무엇인지에 
대해 질문했었습니다.

**synth**
큐브 위성 발사를 위한 비용은 얼마입니까? 300만에 200?

**mike**
FPGA과 아날로그 및 GIO, PWM이 내장된 듀얼 코어 ARM이 있습니다.

**synth**

> 그는 스카이코인 노드를 돌리기 위해 필요한 사양이 무엇인지에 대해 질문했었습니다.

이상적으로, 우리는 1GB의 램 보드가 장착된 2Ghz arm 보드 수준으로 유지하려고 합니다. 

**mike**
1기 위성 당 마이크 50K 비용이지만, 비용이 많이 내려가고 있습니다.

**synth**
스카이코인은 매우 경량화 되어 있습니다.; 비트코인이나 이더리움보다 자원 사용량이 훨씬 적습니다.; 대역폭 사용량은 10KB/s * 10KB/s 미만입니다.

**thrice.pi**
감사합니다...네, 전혀 그렇게 들리지는 않지만요.. 답변을 주셔서 감사합니다. @synth 어쩌면 제가 이 답변을 놓쳤을 수도 있지만요. 
다음 ico가 열리는 시기는 언제입니까?

**mike**
그리고 현재의 Bitseed V2에서 아무런 문제없이 실행할 수 있습니다. 1Gb RAM, 1G 이더넷 및 SATA, 4Gb eMMC가 탑재된 듀얼 코어 Arm입니다.

**synth**
다음 ICO는 단지 홍보용이지만, 제 생각에는 7월 20일입니다. 그리고 그것은 가장 큰 거래소 상장 작업과 마케팅 및 PR  등을 실행하기 전에 시행됩니다.
듀얼코어 arm은 비트코인와 이더리움을 실행할 수 있습니다.; 이것은 매우 놀라운 일입니다.; 이더리움은은 CPU hog여야합니다.

**thrice.pi**
얼마나 오랫동안 열립니까?

**michaelthecryptoguy**
역시 techbytes는 좋은 질문을 해 주었습니다. >>>>> 스카이와이어 노드나 다른 코인의 마스터 노드 같은 합의 노드를 실행하려면 스카이코인을 사용해야 합니까?

**synth**

> 스카이와이어 노드나 다른 코인의 마스터 노드 같은 합의 노드를 실행하려면 스카이코인을 사용해야 합니까?

아니오, 우리는 몇 종류의 프리미엄을 가지고 싶습니다. 만약 당신이 코인을 지불하지 않으면, 노드는 무료사용 계층에 대해 대역폭의 20%를 할당할 
것입니다. 그러나 지불하는 경우 지연이 없으므로 서비스와 속도는 훨신 좋아집니다. 하지만 만약 사람들이 지갑에 코인이 없다고 하더라도, 
우리는 사람들이 서비스나 네트워크에 접근할 수 없도록 하는 것을 원하지 않습니다. 그러나 우리는 프리미엄 계층을 위해 자원사용률의 제한치를 
설정하는 것이 필요하며, 그로 인해서 제어가 불가능하거나 네트워크 정체를 일으키지 않을 것입니다.

**michaelthecryptoguy**
:훌륭합니다.:

**thrice.pi**
@synth는 홍보 목적의 7월 ico에 대해 언급했는데 ... 이것은 Mike가 "스카이코인은 원래 계획대로 메쉬 노드를 설정하고 등록하는 노드 보조 계획이 
있습니까?"라는 질문에 관한 것 같습니다.(편집됨)

**synth**
네트워크 상의 사람들을 모으는 것은 쉽습니다.; 아무 것도 하지 않고 말입니다.; 그 다음 그들은 나머지 사항과 최적화 방법에 대해 파악하고
32노드 클러스터를 설정 및 코인 로드, Linux를 학습하여 CLI를 사용하고 10Gbps 업링크 및 해당 이웃 라우터 및 그들의 지붕 위에 있는 Wi-Fi 노드로 
연결되는 물리적 케이블이 있는 채굴자가 됩니다. lol

**thrice.pi**
lol

**mike**
그리고 Orange Pi PC를 사용하는 것 같네요. 커넥터 포트 중 하나는 USB, 다른 이더넷입니다. 
http://www.orangepi.org/orangepipc/ . 이것들은 멋진 카드입니다. orangepi.org orange pi pc - Orangepi

**synth**
결국, 만약 당신이 40 Ghz 및 지향성 안테나, 위성, 드론이 있다면 또는 도시 간의 장거리 통신 또는 트래픽 릴레이를 할 수 있습니다.
나는 우리가 이 일을 할 수 있다면 "채굴자들"과 하드웨어의 혁신을 이룰 것이라고 생각합니다. 우리는 유기 반도체 잉크로 위상 배열 및 프랙탈 안테나를 인쇄하는 박사 논문을 쓴 사람이 있습니다. 그는 이미 회사에 스카이코인 "채굴용" 하드웨어 안테나를 설치하기를 원합니다. 
그러나 이 혁신을 시작하려면 소프트웨어에 많은 작업이 필요합니다.

**mike**
네, 그게 바로 우리가 Bitseed에서 기다렸던 것입니다. BTC 풀 노드를 평균 시간에 했습니다.

**thrice.pi**
스카이코인은 엄청난 코인이라고 생각합니다.. 그러나 일반적인 사용자가 자유롭게 사용하는 것이 어려울 수도 있습니다. 
ark와 같은 무언가가 스카이 코인의 관문으로 사용될 가능성이 있다고 생각하십니까? 그리고 일반적인 사용자가 ark 네트워크처럼 사용하기 쉬운 네트워크를 이용하여 스카이 코인처럼 광범위하고 복잡하며 혁신적인 서비스에 연결할 수 있습니까? @synth (편집됨)

**synth**
나는 완성파일을 제공할 것이며, 따라서 당신은 대량 제작을 시작할 수 있습니다. 우리는 공장이 없으며 한 번에 30대를 조립하는 것이 어렵습니다.

**thrice.pi**
만약 이 문제가 해결되었면 죄송합니다.. 저는 눈 깜짝할 새에 이 엄청난 질문들을 놓쳐버렸네요.(편집됨)

**mike**
안테나는 그래핀 잉크로 인쇄 할 수 있으며, 정상적인 경우 큐브셋 호환 폼 팩터에서 200dB 이상의 이득을 얻을 수 있습니다.

**michaelthecryptoguy**
이것은 정말 도움이 될 것입니다. : 댄싱 : 제 3 세계 국가의 사람들은 ; 태양이 됩니다.: (스스로:이것:보유) 금융 서비스 및 통신 회사 : 진부함:: 좋은직업 :: 새로움: 이제 우리는 그들에게 스마트폰을 보급하는 길을 찾아야 할 것입니다. : partysaurus :: tophat : (편집됨)

**mike**
그렇게 하는것이 아주 좋을 것입니다. 조립 소요 시간이 훨씬 짧으면서 비용이 적게 드는 포장을 생각해봐야 겠습니다.
makerbeam을 이용하는 것이 좋아보입니다.
스토리지가있는 고정 노드와 메쉬 네트워킹 기능을 갖춘 오픈소스 모듈식 모바일을 통해 안전하고 암호화된 네트워킹으로 세계적인 보급률을 달성 할 
수 있습니다.

**synth**
네, 고정노드, 이동 노드는 많은 문제를 야기합니다. 스카이 와이어는 사람들이 이동하는 공간에서 "모바일 애드 호크 네트워킹"이 아닌 지점 간 
세그먼트를 통해 실행되도록 설계 되었습니다.

**arc-over-water**
출시된 기본 프로그램 제품이 있습니까? 현재 단순 지갑에 불과한가요?

**mike**
그래서 라우팅 테이블이 자주 업데이트 되지 않습니까?

**synth**
https://github.com/skycoin 에  다양한 애플리케이션이 있습니다.
https://github.com/skycoin/bbs 작업이 현재 진행중입니다.
이제는 라우팅 테이블이 새로운 연결에서만 변경됩니다. 그래서 당신은 공개키에 ~ 10 개의 연결을 만들고 어떤 경우에는 일부를 소멸하고 새로운 연결을 
생성합니다. 그리고 경로와 전송 방법에는 중복이 있습니다. "다중 라우팅"은 노드 간의 직접 연결이 10 초 이상 걸리는 빈도를 줄입니다.
최적화되어있으니 변경하지 마십시오. 기본 물리적 연결에 대한 변경, 업데이트 충돌 발생 및 네트워크 토폴로지 변경(최소화해야 함)에 대해서.
연결 해제 또는 라우트가 있거나 연결이 설정된 경우 네트워크 토폴로지가 변경되지 않고 대역폭에 관리 오버 헤드가 없습니다.
단거리, 모바일 애드혹 라우팅은 BATMAN과 같은 다른 프로토콜에 의해 처리되어야 하며 WIFI 핫스팟과 같은 고정 인프라, 도시 간 광통신, 이더넷 케이블 등은 스카이와이어 항목에 의해 처리됩니다.;그래서 만약 당신이 커피 숍에 들어가서 30 분간 연결하면 괜찮습니다.; 하지만 5 초마다 다른 핫스팟에 
연결되는 거리를 운전하는 경우에는 이를 위해 설계되지 않았기 때문에 "모바일"을 위한 또 다른 프로토콜 계층이 필요합니다.

**mike**
그래서 노드는 움직일 수 있습니다. 만약 송신이 중단되지 않는 경우, 빔이 통신을 방해하지 않도록 충분히 빠르게 움직일 수 있는 한 안테나의 빔을 생성할 수 있습니다.

**mike**
그래서 노드는 움직일 수 있습니다. 만약 송신이 중단되지 않는 경우, 빔이 통신을 방해하지 않도록 충분히 빠르게 움직일 수 있는 한 안테나의 빔을 생성할 수 있습니다.
업데이트를 참조하십시오. 그들은 일부 중단현상이 발생해도 문제가 없다고 합니다.
미니 셀 타워 및 액세스 포인트와 같은 기능을 하는데는 문제가 없지만 휴대용 모바일 구축은 다른 프로토콜입니다. 만약 셀에서 셀로 이동하는 경우에는 말입니다.

**synth**
네, 단계적 배열은 괜찮을 것입니다.; 또는 신호가 두 번째로 중단되었거나 신호가 매시간 끊어지고 다시 돌아오더라도 네트워크 토폴로지의 근본적인 
변화가 더 성가신 문제입니다. 전체 네트워크에서 라우팅에 관여하는 모든 사람들에게 통보해야 하기 때문입니다.
따라서 CXO를 통해; P2P(peer to peer) 업데이트를 실제로 수행해야합니다. 
결국 네트워크는 각 노드가 현재 인터넷에서 정상적인 방식으로 분할된 하나 이상의 라우팅/가입 도메인에 속하도록 세그먼트화 되어야 합니다. 
두 사람 간의 최근 중단 홉 수는 ~40 또는 80이어야 하며 또는 예측할 수 없는 숫자일 수 있습니다.;
스카이코인에서 그것은 4 또는 최대 7이 될 것입니다. 집에서 주변 이웃, 도시, 도시/국가 그리고 다른 목적지까지 말입니다.
그것은 40 개의 물리적인 홉 (hop)으로 나타나지는 않을 것이며, 그것은 각각 개별적인 혼잡을 가질 수 있습니다.
위상배열의 이점은 다음과 같은데, 당신은 지금 당장 당신의 지붕으로 신호를 던져 당신이 연결하고자 하는 사람을 검색할 수 있습니다.;
그 다음 지붕에 올라가거나 다른 작업을 할 필요 없이 다른 사람 또는 좋아하는 사람과 연결할 수 있습니다.;빔 신호는 소프트웨어로 조작합니다.
나는 BBS와 VPN을 좋아하는데, 우리가 그것을 구동하기 위해서 새로운 물리적인 인터넷을 구축할 필요가 없기 때문입니다.;
우리는 단지 기존의 인터넷을 터널링하고, 그것은 유용합니다. 기존 인터넷의 하드웨어 대안이 개발되기 위해서는 수 년이 걸릴 것입니다. 
사람들이 한 달에 100,000 개의 노드를 설치하고 하루에 1% 씩 성장하고 있어도 기존 인터넷을 대체 할 수 있을 때까지 10 ~ 15 년이 걸릴 것입니다.
많은 장비가 있고 성장률이 엄청나더라도, 많은 시간이 걸릴 것입니다.

**mike**
네, 이것은 제가 좋아할 만한 것이네요. 포인팅 안테나보다 자동 설정 안테나가 훨씬 쉬우며, 노드에 저주파를 사용하여 GPS 좌표를 전송하여 서로 위치를 결정한 다음, 가능한 가장 높은 주파수 범위를 서로 연결하는 것이 좋을 것 같습니다.

**synth**
the VPN will be big application; hardware vpn, whole house VPN; you plug it in and it VPNs your whole house and all your connections
the ISPS are allowed to sell all the data they collect now
and you can start hardware blocking the IP addresses for ad servers and tracking servers and so on; and different vpn end point for each device on the lan and be able to rotate them out automatically
what will happen, is that all the torrent sites and communities will be driven underground; and when that happens, the downloads will eventually be blocked or slowed by ISPS and you will need a "new internet" to really get a lot of the content that is available to people now.
Five years ago, there was no point in doing this. Today the motivations are emerging, that will drive people to something new
and another thing is that reddit has been overrun with bots; controlling all the upvotes and content now. And corporations have completely taken over and subverted facebook and twitter.
People are going to be looking for decentralized platforms and there will be a mass movement to the platforms that can solve the bot manipulation problem, the shilling problem and the company owned by corporate money whore sellout problem.
so there were attempts at a building decentralized twitters and facebooks, but five years ago there was not a need; now people are ready to siwtch and the technology is ready.
the skycoin project is building the base layer, then the communities are building their own projects. We are just giving them the tools.

**mike**
Yes, like as an example, twitter made my sign-up email public, had no idea, was getting spammed all the sudden, finally found out why when I went to twitter to stop getting multiple copies of a privacy notice.
Would very much like to bridge skycoin with Ark, so Ark runs on top of this VPN, and advantage is that your VPN is trustless, or at least much more decentralized than relying on a single VPN provider, which is 100% reliant on trust.

**xano**
How do you feel the incredible potential for illegal activities will affect the future of Skycoin and mass adoption?

**charles**
I also don't quite understand how skycoin solves the bots on reddit

**xano**
Almost everyone loves free movies, series and music, but what if ISIS starts using it for example

**synth**
now, on twitter; for instance hillary clinton campaign paid twitter money for "brand management" and if 300 people you follow said something negative about her, you wont see any of the tweets. And 1 person in 4000 says something positive and everyone in the that persons followers, will see the tweet in the feed!
The companies are controlling what people see and what information is allowed into their feeds. Its not organic anymore. Its not based upon your preferences. It is based upon making the platform friendly to advertisers, who can pull their money out. They are pushing social agendas even and requiring the companies they are giving money to, to censor particular people and movements, to keep the advertising money.
Even Google is being forced to comply with these demands. Fortune 500 pulled out 700 million/year in ad revenue and then google agreed to censor search results to please the advertisers. And then they are threatening them with fines in the EU unless they comply and serve the governments and corporations.
Decentralized social media, means that you own your own data. It means that you control on your computer, the algorithm used to sort and prioritize your feed. Instead of allowing it to be controlled and manipulated by a third party, who is a whore for money trying avoid being fined by the EU and groveling before soap companies threatening to pull their ad money out, unless they censor things.
yes, ARK could use skycoin network for block and transaction distribution. And could use it for networking, to avoid blocking.
And ARK could be deployed as a node in the same framework as skycoin. in the skycoin clusters.
There is https://github.com/skycoin/viscript and we can add ARK here. This is a cross platform CLI, and application launcher and for cluster management eventually.

**mike**
thanks! will post to our devs. we have and are adding a lot of API's and CLIs for different languages.

**synth**

>I also don't quite understand how skycoin solves the bots on reddit

It is outside of skycoin project, but the people building the BBS has a really cool filtering algorithm. Everyone is identified by their public key and can build out a web of trust. And its like page rank for users.
Its a decentralized type of moderation, that is automatic.
is ARK in golang?

**jarunik**
Ark chain is in Javascript but we got a golang api.

**arc-over-water**
Why golang over rust or scala?

**mike**
Ark core is written in node.js , may be ported to go. There is a go api/cli being written, by @chris I believe.

**arc-over-water**
when will there be a lisp coin platform :slightly_smiling_face:

**mike**
golang is done? nice!

**boldninja**
https://github.com/ArkEcosystem/ark-go GitHub ArkEcosystem/ark-go ark-go - Ark GO client for ARK.io blockchain ecosystem #golang #ark #blockchain

**mike**
lisp - that would be fun! Continue to be amazed lisp is still around, but popular for machine learning apps. yes, we need lisp added, can you do it arc-over-water?
lisp seems to have good function for parallel processing but don't know details myself.

**arc-over-water**
now there is Shen.. http://shenlanguage.org/

**synth**

>How do you feel the incredible potential for illegal activities will affect the future of Skycoin and mass adoption?

The people selling drugs will love skycoin. Bitcoin was worthless until people could buy drugs with it, then it was money and it went from $0.01 to $1000 in a year.
When the internet was created, the first thing people were doing was downloading porn. When bitcoin was created the first thing people were doing was buying drugs and guns.
ISIS does not need skycoin, because they are using xbox messanger and facebook messanger. They do not need crypto. Every terrorist attack means budget increases, so the government loves ISIS. Terrorism is big money and the more terror, the more money there is to make. People are making too much money off of ISIS for them to get rid of the problem any time soon.
Pedophiles were also the first ones to adapt stenography, i2p, tor, tails and bitmessage. They are always the first ones testing out any new crypto stuff. You should look at the logos of the stenography apps and you can guess what kind of people wrote these applications.
Even two years, before skycoin was launched the intelligence and money laundering people were already showing up and giving lists of requirements for scrubbing or hiding metadata.
If I was building the next silk road I would be looking at tech like skycoin is building. I think everyone has had that idea.
We really cannot control what people are going to do with this. Its just inevitable progress and its going to happen whether we do it, or maidsafe does it or someone does it. Its going to happen. (edited)

**mike**
looks interesting. have you seen julia, https://julialang.org/ . very impressed with its benchmarks, comparable to go
think the best way to end terrorism is to end foreign interventionism. Last I knew, Switzerland doesn't have a problem with terrorists.

**arc-over-water**
killary and obomba

**michaelthecryptoguy**
Sad but true.

**mike**
and the bushes

**synth**
uploaded this image: Screenshot from 2017-06-29 14:42:25.png Add Comment

**synth**
uploaded this image: Screenshot from 2017-06-29 14:41:55.png Add Comment

**arc-over-water**
fake news on an amazing level... sandy hook.. 911
moon landing... Stephen Hawking...
anyways..

**charles**
North Korea also does not have a problem with terrorism :)

**arc-over-water**
Sky! the limit

**mike**
don't even have to go to that level, just the current ongoing farce about Russian intervention in the election and supposed ties to Trump team members. War is the health of the corporate state.

**synth**
terrorist attacks are now advertising events for nike; they are fighting each other for who gets the product placement in the latest ISIS attack. It keeps people glued to their televisions and otherwise people would not watch the news. Even terrorist attack keeps people on the television and the fortune 500 fight each other, to get the ad spots for the people glued their television.
The governments and companies race in, like sharks with the latest "surveilence" bill to get the governments to buy billions of dollars of useless equipment from them. The government agencies all rush in to influence the press and get budget increases passed.
Its just insanity. They only care about money.

**mike**
it would be very inconvenient to improve relations with Russia for those making money and expanding power over escalating global tensions.

**arc-over-water**
wasnt the first main scandal trump attack that he weed on some prostitutes in Russia. OMG

**synth**
they have oil companies and russia produces oil; so hey want any execuse for "sanctions" to force people to buy their oil instead of russian oil. They would do a war, just to stop any Russian oil pipeline to Europe.
It just about money.

**arc-over-water**
Putin is actually kicking some ass with his speeches the last years.

**synth**
if russia gave me free prostitutes, I would pee on them too, lol. Why not? (edited)

**mike**
don't forget Pussygate - the press sat on the tape for 10 years until 3 weeks before the election, instead of during the primaries.

**arc-over-water**
crazy shit out there...
time for crypto to shine..

**xano**
I just wonder how services like mega would have ended up with Skycoin

**synth**
the "Y2K" was also excuse, to sell tens of billions of dollars of "upgrades" to government and corporations. They told them "give us your money or the sky will fall".
terrorism is the same story, its just turned into a money making scam. 90% of the surveilence crap is just companies finding excuses to lobby the government to buy over priced equipment, so they can make money. They do no even know what to do with the data they collect. They are doing insider trading and rigging markets and all sorts of crap with the data and then panicing when people start using HTTPS because its harder for them to keep making money the same way.

**arc-over-water**
Mega2 is about to show its prototypes

**synth**
you have mom and pop local police departments, buying $150,000 string ray cell phone interception equipment that is NSA level, who could not even afford it, but its paid for out of 10 billion dollar DHS "terror" fund to buy useless equipment for local police. To "fight terrorism". Its really a joke.

**arc-over-water**
Sky list of aims over the next two years?
Next ICO cost and how it will be released?

**synth**
people know that companies like apple and goolge are required to hand over all their data to the government. including messages, so why would anyone use imessanger or icloud?
So they are staging fake events with "police cant break the 4 digit pin on an iPhone and its unbreakable" when they can actually trojan the phone from the carrier, etc and have all sorts of insane mandatory backdoors.
So we are heading towards a decentralized internet and these new apps, as people get sick of being tracked like animals.

**michaelthecryptoguy**
@synth What is your background? Can you tell me a little about your prior experience, regardless of what area it was in? (edited)

**synth**

> Sky list of aims over the next two years?

Get meshnet working Get BBS and first demo apps working Get VPN working and get it to users List on more exchanges Build up community Improve the wallet, fix website, translations into more languages ec

**arc-over-water**
Also the two Chinese guys who wrote the technical whitepaper, the scholars, are part of the team?

**synth**
@synth What is your background? Can you tell me a little about your prior experience, regardless of what area it was in?
I did a lot of things. video games, hedge fund/finance, crypto, investment stuff etc... Now am I a sort of project manager.

**charles**
How will the price of skycoins be determined for the next ICO, I, suppose it cannot be above market price, else people would not buy it, but too far below would depreciate the coin

**arc-over-water**
do they want high price at this point or well even distribution to the best placement of people?

**synth**

> Also the two Chinese guys who wrote the technical whitepaper, the scholars, are part of the team?

One of the chinese guys has nothing to do with it. He is a professor that put his name on paper his graduate student published. And now the professor wants to hide the paper, because he thinks the chinese government is cracking down on bitcoin; but he is wrong and the government doesnt care and the paper is in english so they cant read it anyways.
And the other one is a core ETH developer. Chen was core ETH and wrote the golang implementation of Ethereum. He is not very public and does not want to be in spotlite or bothered.
most of the contributors for skycoin are in the background or hiding actually (edited)
many of the ETH people are all whoring themselves out to advisor boards to various tokens, or dozens of tokens and ICOs; but most of the serious crypto people are very private and hiding themselves. They do not want to be known, do not want to promote or advertise themselves and they are in the background.
Or they have too much money already and just want to hide. They are also lazy because they do not have to work anymore, or they are busy with other things.
they also want to avoid taxes and being targetted for theft and do not want attention from government
skycoin cannot have a "Team" or "Advisor Board" on website, because we asked everyone and no one wants to be public or wants to be in a public position....

**arc-over-water**
yes best to live in a country your not citizen of and earn money from a country your not living in... Been doing it for ten ears, way less stress, (edited)

**synth**
many early bitcoin people, who identified themselves publicly on twitter; they cannot travel to brazil or certain countries without risking being kinapped and ransomed for money
lololol

**arc-over-water**
vitalic knows kung fu maybe,,, well he speaks Chinese..

**charles**
Do you think skycoin not having a public figure will negatively affect adoption?

**arc-over-water**
i think it has.. 6 years on and quiet forums and slack

**synth**
we can buy public figures or an adviser board; but they would not have anything to do with project except to put their name on it to create confidence for public; which is what all these advisor boards really are

**arc-over-water**
in the background assuming tek development.
Next ICO cost and how it will be released?
github is always active...

**synth**
i really do not know
about the next ICO

**arc-over-water**
ok

**synth**
it is around the 20th of next month. and will be 1% to 10% of the skycoin. I am not sure the exact number is set
and it will probably be a fixed price

**dr10**
this ama is a marathon :trollbounce: nice!

**arc-over-water**
how much of the 100 million is obligated to your team and the people who funded it?

**synth**
but then followed by a weekly auction or second priced auction for a fixed number of coins, that will occur every week for 8 weeks; but not sure how many coins or if it will actually happen

**arc-over-water**
so if its a high price it is 1% and low price it could get to 10%

**synth**

> how much of the 100 million is obligated to your team and the people who funded it?

The people who funded skycoin, did not receive anything for it. They have no entitlement to the coins.
they had to buy in at ICO like everyone else. Even the developers working on it, had to buy in.

**arc-over-water**
ok so they have already been looked after in the 10c ICO round

**synth**
i think the next ICO is mostly marketing event, and to "get it over" with. We are in a bubble now, so we should raise money now, before the ICO bubble pops. Is what people are telling us.
we cannot spend more then 50 million, so selling an insane number makes no sense. 10 to 15 million is probably reasonable, for next 3 years. And that is with a really good full time marketing team, and trippling number of developers AND funding several parrallel hardware projects.

**mike**
My approach to Skycoin is regardless how much of a financial return it might provide, it is an investment into producing a future I want to see.
Also look forward to earning it by running nodes.

**arc-over-water**
So that could be you release 10,000,000 coins and get $10,000,000 dollars for your covering expenses next three years

**charles**
Can a person with limited technical capabilities run a node?

**arc-over-water**
or $20,000,000 as it goes

**synth**
the people who are going to pump the coin, want us to sell off as much as possible. They are pressuring us to do that.
However, if we sell fewer coins, then the price per coin will be higher.
If we only sell 10 million in coins, then the price can go up a lot higher than if we sold 500 million in coins.
I think EOS is going to raise a billion dollars and I have no idea what they will with the money, except use it to buy EOS and drive the price up or some scam. They are not going to spend it on development. lol
> Can a person with limited technical capabilities run a node?

eventually, yes. maybe not right now. after tutorials, yes

**arc-over-water**
EOS seems like it is trying to go bear bones and not be as complicated as ETH...

**mike**
I think it is smart to hold a lot for distribution to node operators as a replacement to mining for a good distribution, also selling some to have distribution among those who are interested but not technically inclined to run nodes.

**synth**
So that could be you release 10,000,000 coins and get $10,000,000 dollars for your covering expenses next three years
The coin price is like $4 or almost $5 at high. It will be at $5 by ICO I think, atleast. The market cap has doubled every 40 days, for a while now.
10 million coins at $5 per coin, is 50 million.
We have to distribute coins via the skywire nodes, to make it fair; because ICO is not a good way to get coins into the hands of users. Its only good for fund raising and for whales.
We decided that we will distribute most of the coins to users and just use sales to whales, to fund development.

**arc-over-water**
there must be ways to spread to diverse groups the 10,000,000 coins?

**synth**
the problem is that all ICOs end up going to less than 20 whales

**arc-over-water**
every member of a altcoin slack gets a coupon invite
If an ICO knows their customer that can be prevented..

**synth**
there are people who own a large percentage of ETH and they want to diversify; they can gamble 20 million in an ICO and could make 50x more, but if they lose it, then its a slight loss; they have so much ETH that they cannot even sell it or convert it, without tanking the market

**arc-over-water**
in one day every altcoin slack member of every altcoin could get a btc address used once in their pm, allowed a max amount sent etc..

**synth**
yes, ideally, that might work
we have been doing OTC sales at market price; with a cap of 10 BTC and that works well

**arc-over-water**
do the OTC reflect in the blockchain? (edited)

**synth**
but we have single whales that want to put in 700 BTC and each one individually, is larger than whole individuals doing the OTC sales
OTC is "over the counter", or direct sale; when people private message a developer and ask to buy

**arc-over-water**
ok so private sales are happening

**mike**
uploaded and commented on this image: TEC chart.png 1 Comment Here is a sample method based on power law for pricing I have planned for Ark based Token Exchanges for projects, including funding Ark/Skycoin based nodes. As more as sold, the price increses by a power law so people can enter at the irsk and expected ROI combination they feel comfortable without being pressured into hasty emotional decisions by FOMO.

**mike**
*irsk=risk
so entering on any part of the curve looks the same as any other part.

**synth**
hmmm
how does this work?
the more money you put in, the more you pay?

**arc-over-water**
but as you do these OTC sales it reflects here in distributed? http://explorer.skycoin.net/blocks

**mike**
here is a link to the spreadsheet, has the formulas and table of calculations for the graph, https://docs.google.com/spreadsheets/d/1en9lqzBIuHgp0-Q3ohoq3yJUe1lJcOK9U4bF2TiXZew/edit?usp=sharing
yes, the more that is put in, the higher the price.
it will take some experience to determine the best parameters to prevent instant sell-off while not stalling the exchange indefinitely, and different project might be best suited for different exchange rates over time period.

**synth**
we have a really good strategy now
We can distribute coins to top content producers on the BBS
to people doing bountries (like skycoin logo, sticker design etc)
to people who want to do development (mobile wallet etc, some features for bbs and bug fixes)
Then massive substained distribution, over time to the people running the skywire nodes.
Then disribution also to nodes hosting content on CXO.
Then distribution to people coming on to platform who are bringing user communities with millions of people (we have been talking to these people for years and they do not have real developers, so we have to help them; they only have web designers and curators and community managers but cannot actually develop anything new).

**mike**
like a long term term ArkSpace project for space exploration and development will be sold over a lot longer time frame than funding an index coin bridged to Ark.
yes, and either way, the project can award blocks of tokens to contributors other than just for money.
I'm a fan of the Slicing Pie method.

**arc-over-water**
Ok so your saying it will be between 1%-10% next month to get funding and start the marketing campaign. Then after that distribution then there are monthly small releases of ICO and the majority being bounties for services rendered. and nodes etc

**mike**
http://slicingpie.com/ Slicing Pie Perfect Equity Splits for Bootstrapped Startups Slicing Pie is a formula that allows founders to create a PERFECTLY FAIR equity split between founders, investors, partners and employees. (92kB)
Skycoin is very similar, but doing it manually with adjustment.

**synth**
yes
what i am interested in, is if we can block the BBS up and get alot of users with the incentives
every dollar in coins we sold over OTC, drove the skycoin market cap up $4
we would sell coins, then price explodes the next week; because people promote it on twitter and blog about it
skycoin needs to get on more exchanges

**synth**
I have to sleep now. LMAO. We should end AMA soon

**arc-over-water**
cool thanks for your time... haha 3.17 am here

**synth**
4 hours?

**dr10**
XD

**synth**
is there an archive for the AMA?

**dr10**
reddit hopefully :joy:

**michaelthecryptoguy**
Thank You for taking your time to answer everything in complete detail. It was nice that you cared enough to make sure everything was answer very thoroughly.

**boldninja**
@michaelthecryptoguy can you copy everything and make it reddit friendly?
thanks @synth for taking the time for this AMA it was :mindblown: really interesting stuff

**techbytes**
오늘은 마라톤 세션이었네요.

**michaelthecryptoguy**
I sure can. As long as jarunik hasn't already started. (edited)

**mike**
synth와 함께 해 주셔서 대단히 감사합니다. 다음 기회에 다시 참여해주신다면 감사하겠습니다.
저는 지속적으로 스카이코인 슬랙을 확인하여 새로운 소식을 전할 것입니다.
[skycoin.slack.com](https://skycoin.slack.com)
가까운 미래에 스카이코인이 Ark와 함께 한다면 더 좋겠습니다.
