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
So Skycoin would act as a sort of global decentralized cloud server to build on top of.
To communicate, it is more like sharing encrypted files to selected recipients than it is sending messages or hosting sites on a specific server.

**synth**

>Are you a corporation or foundation or charity? Registered? I am not sure i have seen anything about who you are? What is the dev team size? Background?

I think there are over ~60 people who have worked on Skycoin or have made major contributions. Its really a project from the darknet.
Many of the contributors are anonymous. Some of them have security clearances and were in the military industrial complex and one of them worked at the San Diego Naval Defence Research Lab and a lot of the idea for the networking protocols came out of public sector academic researched, funded from there.
We also have a lot of very very early Bitcoin people, hardcore crypto people that predate Bitcoin and an Ethereum core developer, etc..
On the Chinese side we have an early investor in Alibaba and telecom investor. And are doing pilot with china aviation group (owns four publicly traded airline companies) and apparently now Sinopec (which is 2nd largest publicly traded corporation in world).
Then we have people who are part of israeli and US intelligence and are probably doing some sort of money laundering or phychological operations background, who just showed up for some reason. This group seems very interested in the "applications" of these coins and how to improve tranaction privacy and the specifics of the CoinJoin protocol implementation. We got a lot of advice from people experienced in forensic accounting and what they wanted to see and where they felt Bitcoin was deficient and where it leaked metadata.
Then a bunch of PHD level people doing research into distributed database consensus algorithms and another group doing programming language research.
Then a lot of people from the deep darknet, anon, frog twitter and cipher punks and bitorrent communities. (really should be listed as two seperate groups). And people from the Russian darknet community. We have like eight Ivans. (edited)
> I see Skycoin as essentially replacing TCP/IP and providing mesh network type functionality at the hardware level, Ark would run on top of it as a top level application layer.

Yes. The key functionality is two things - connecting to people by public key (networking) - distributing self validating, immutble data peer to peer (transactions, blocks etc... content addressible storage)
And you can build almost anything on those two building blocks. The whole internet will eventually be rewritten on top of those primitives and it will replace many of the existing protocols.

**arc-over-water**
Who is the entity that is funding this? I think you have done 2 ICOs? How much did you receive? The first was 10c and the second was @ 50c per coin, released 6 million, is that correct?

**samuelvihollandia**
Are you planning to enter a different exchange market soon?

**arc-over-water**
Have you personally been in Sky from the start? What members have? Who allocates the ICO money etc... I hope you understand that decentralization with investment is a two edged sword, we invest in people but we cannot know these people.... So... we question.. (edited)

**thrice.pi**
with all these outside parties that helped to build skycoin and bring it where it is today who are the main core team who will help to keep all these cool features running. Will these outside parties be recruited for the long haul?

**synth**

> Who is the entity that is funding this? I think you have done 2 ICOs? How much did you receive? The first was 10c and the second was @ 50c per coin, released 6 million, is that correct?

The people who funded the project for the first four years, were early bitcoin and deep crypto people; who were unhappy with the fact that Bitcoin and the other alts did not seem concerned about the core issues at all. They gave us over 1200 bitcoin I think, over several years and did not ask for anything in return.
The early Skycoin devs were doing academic research, architecture and new algorithms. Prototyping and simulation. The later stage people were more project managers and doing implementation.
We did four ICOs for small amounts, to fund development and to allow developers working on the project to buy in. The first ICO I remember was at $0.10 per coin and the price now is about $4.00 per coin, so its up ~35x or 40x, but when you consider the Bitcoin price going from $100 to $3000, the increase has not been so much. lol (edited)

**arc-over-water**
With the price up 35x in about 1 year, is it not now time to cool the run up and release another ICO? At what amount of coins released and what procedure?

**mike**
Would Intel Edison or Joule, or Samsung Artik 10 work well as a Skywire wireless node? They have 2 Gb-8 Gb RAM, 8-64 Gg eMMC storage, 802.11n wireless, bluetooth, and some with Zigbee?

**synth**

>Have you personally been in Sky from the start? What members have? Who allocates the ICO money etc... I hope you understand that decentralization with investment is a two edged sword, we invest in people but we cannot know these people.... So... we question.

I think there wer three different groups that merged together in first three years, that had similar objectives. Because the code was in different language. There was python, C code and then eventually golang and the golang code became the basis for the current codebase.
The way the coin allocations work, is that it requires unamimious consent for releasing coins and it has to be for a specific, ear marked purpose and can be blocked by any of the devs.
Then there is a pool of coins in bitcoin for various project managers to allocate. And that is an operational fund for paying developers, contractors, marketing etc. Then different people have different responsibilities.
Then we also have corporate funding and sponsorship and some companies paying our full time devs etc, which helps a lot.

**arc-over-water**
Silicon Valley (TV SHOW) recently had their decentralized web running on a network or refrigerators? So i would guess, smart phones, smart gadgets? Home gadgets etc could add services and receive rewards from Sky?

**mike**
best would be a totally open source and publicly audited manufactured system on a chip for the nodes to prevent any backdoors. Even chip designers now don't really know what they're putting into the chips since they just drag and drop black boxes known as IP cores into the ASIC designs.

**synth**

>With the price up 35x in about 1 year, is it not now time to cool the run up and release another ICO? At what amount of coins released and what procedure?

I think the Skycoin price has been doubling every 40 days, for as long as I can remember. However, it will still be years before it is in the top 20, its still a long way to climb. It took bitcoin years to go from 0 to $1, even though it was growing at 1% per day the whole time for six years.

> best would be a totally open source and publicly audited manufactured system on a chip for the nodes to prevent any backdoors.

we are going to use arm

**arc-over-water**
IOTA is also working on their own hardware for nodes etc, Trinary asset is JINN

**synth**
all intel and AMD systems have remote management engine backdoors. So they are not safe for storing large amounts of coins.
We also have alpine linux and special version of linux, that is 6 MB and has everything that is needed for running our toolchain. It will not have any binary blobs in the kernel or anything that we cant compile from source. It does not have systemd and does not have gli, but uses musl. And does not have openssl.

**mike**
so looks like the Samsung Artik 5 and 10 can run it no problem, they're ARM based. 25x35x4mm package for the Artik 10, Artik 5 is smaller, less powerful but has 2 separate antenna ports, nice for mesh networking with an omni and a directional antenna.

**earlyarkinvestor**
how does Ark compare to Lisk?

**synth**
uploaded this image: 1923810435.jpg Add Comment

**earlyarkinvestor**
isn't Lisk trying to achieve interoperability between blockchains as well

**synth**
uploaded this image: 1433594905.jpg Add Comment

**synth**
uploaded this image: 1432540863.jpg Add Comment

**synth**
uploaded this image: 2049465686.jpg Add Comment

**mike**
nice! looks like an ARM based server rack
let me know if you need any help with it, see you're on solidworks, which I run as well.

**synth**
this is the skycoin cluster; it has 8 CPU boards; 4 cores per CPU, 2 GB of ram per CPU and 64 bit ARM processor. Only one program will run on each individual board, so there is compartmentalization and a physical gap so that compromising one process on a system does no allow all other processes on the system to be compromised

**mike**
looks like 2 ethernet ports per board.

**synth**
and the hardware does not have the qualcom backdoors and is actually chinese equipment; and the backdoors are normally at the kernel level because they are not at hardware backdoors yet
lol

**mike**
do they have SATA ports, maybe M.2 for storage?

**synth**
and we will hav an ARM openwrt router eventually too
this model does not have SATA, but we have a model with SATA; you could hook up 16 2 TB drives, lol and download half the piratebay to your cluster (edited)
the skycoin infrastructure is cluster based and designed for running across +300 computers, with one "node" deployed per computer. Eithe a CXO storage node, or a skywire SDN/meshnet node, or a VPN end point node or a consensus network, or skycoin node, etc. We have multiple node/application types.
so this is a "personal cloud' by itself
its not like StoreJ where you have other people storing your stuff; you are going to have ~5 clusters and 300 computers and can store your own files, on your own internet, on your own hardware. You do not need to go outside of your own network.

**mike**
Have thought it'd be nice to have a board with an array of M.2 sockets to run SSD arrays without all the cables, have the busses shielded in circuit board.

**synth**
yes, i think there will be m.2 eventually
these actually use a microSSD for storage, and its 48MB/s

**mike**
any idea on the pricing on your ARM boards in quantity? We are looking at Intel for Bitseed V3, but ARM would be good to stay with, especially using your boards if there is SATA.

**arc-over-water**
Do you have a general idea of usable functions to be released next in what order? The first release was the Coin and wallet, then the ICOs and can you give a general future with dates if you can

**synth**
the boards are $30 each and the memory for solid state, is actually more than the the cost of the CPU/RAM/board now. Which is sort of insane.

**mike**
so you have microSSD, what's maximum size? we shipping 1with Tb hard drives right now

**synth**
Bitseed mike is going to help with this; so we can pool the boards and do a custom PCB

**mike**
yes, that's where we see the price jumps, is in RAM and eMMC costs.
and it's hard to find low cost boards with SATA

**synth**
try the orange pi
the price goes up 30% for SATA

**mike**
yes, very nice specs.

**synth**
eventually, we will make one that has custom PCB and is a pluggable blade server, I think.

**mike**
I like the Samsung Artiks for the tiny form factor for drone routers, cubesat/picosat possibilities.
but like the fact that you are controlling much deeper down the supply chain with your boards.

**synth**
we only need ram, CPU, then microSD slot; and that is it. so the wifi and all this other stuff is just crap and its junk. We only have communication, storage and computation. So should be minimialist.

**mike**
yes, we use very few of the ports on the pcduino nano, no need for video, audio, IR

**synth**
there is even open source FPGA toolchain and a one instruction computer with subtract and jump if not zero; and if you have ram and a byte array, could even compile down to that; which is trolling, but for signing transactions or something, you could operate at that level.

**mike**
do you have a link for the FPGA. My favorite has been the ZYNQ 7000 series, but this sounds a lot lower cost.

**synth**
I have to ask about the FPGA

**mike**
Blue Canyon uses ZYNQ 7000 for their Cubesat bus.

**synth**
it is education company in shanghai

**thrice.pi**
i dont want to disrupt this communication u and mike have going on cuz its good to see you two discussing these things so please do continue..but i just a simple question that mike actually asked earlier which i didnt see a reply to..he asked what type of spes is needed to run a node for skycoin

**synth**
how much is it for cube sats for launch? 200 for 3 million?

**mike**
it has dual core ARM with an attached FPGA and both analog and GIO, PWM

**synth**

> he asked what type of spes is needed to run a node for skycoin

We are trying to keep to level where 2 Ghz arm board with 1 GB of ram can run it. ideally

**mike**
50K per 1U satellite was the going rate, but that is coming down a lot.

**synth**
skycoin is very minimalist; it much lower on resource usage than either bitcoin or ethereum; the bandwidth usage is less than 10 Kb/s
*10 KB/s

**thrice.pi**
thank u..yes it doesn't sound like much at all..thank you for your reply @synth
maybe i missed this answer but when is the next ico taking place

**mike**
so current Bitseed V2 can run it no problem. is dual core Arm with 1 Gb RAM, 1G ethernet and SATA, 4 Gb eMMC on board.

**synth**
the next ICO is just marketing event, but is july 20th I think
and it is just run up before largest exchange listings and marketing and PR push etc
oh, the dual core arm can run bitcoin and ethereum; that is amazing; ethereum should be CPU hog

**thrice.pi**
how long is it on for ?

**michaelthecryptoguy**
also techbytes had a good question >>>>>Do we need to hold skycoin to run Skywire nodes or consensus nodes like masternodes from other coins?

**synth**

> Do we need to hold skycoin to run Skywire nodes or consensus nodes like masternodes from other coins?

No. We want to have some kind of freemum thing. If you are not paying coins, the nodes will allocate 20% of bandwidth for the free tier
But you wont have congestion if you are paying, so much better service and speed, but we dont want people not being able to access a service or the network if they have no coins in the wallet
but we need to cap the resource usage of the freemium tier, so that it does not get out of control or clog the network

**michaelthecryptoguy**
:excellent:

**thrice.pi**
@synth the ico in july for marketing purposes that u mentioned ...is that pertaining to what mike asked about when he asked "Will Skycoin still have the node subsidy plan for setting up and registering the mesh nodes like originally planned?" (edited)

**synth**
it is easier to get people on network, without having to do anything; then they wil figure out the rest later and how to optimize it and setup a 32 node cluster and load coins in and learn linux and use a CLI and becoming a mining baron with a 10 Gbps uplink and physical cables to their neighbors and wifi nodes on their roof etc, lol

**thrice.pi**
lol

**mike**
so looks like you're using the Orange Pi PC, one of the connector ports is the USB, the other ethernet. http://www.orangepi.org/orangepipc/ . These are nice cards. orangepi.org orange pi pc - Orangepi

**synth**
eventually, if you have 40 Ghz and directional antennas, satilites or drones make sense for long haul or relaying traffic between cities. I think if we can get this working, the "miners" and hardware innovation will be insane.
We have guy who did PHD thesis on printing phased array and fractal antennas with organic semiconductor ink and he already wants to start companies to do antennas for skycoin "mining" hardware; but the software still needs a lot of work before they can start this insanity.

**mike**
yes, that's what we were waiting for with Bitseed, been doing BTC fullnodes in mean time.

**thrice.pi**
it seems skycoin is one hell of a coin..but it may be difficult to use for the everyday user to wrap their mind around..you think there is potential for something like ark to be used as a gateway to skycoin..so the everyday user can use something easy like arks network to link to something so broad, complex and revolutionary like skycoin ? @synth (edited)

**synth**
i will give you the solid works files, so you can start manufacturing these in bulk; we do not have factory and even assembling 30 units at a time is difficult for us

**thrice.pi**
sorry if this has been addressed..i may of blinked and missed it with all these great questions (edited)

**mike**
the antennas can be printed with graphene ink, have over 200 dB gain on a cubesat compatible form factor if done right.

**michaelthecryptoguy**
This would really help :dancing: people in third world countries turn into a :sun: (self :this:owned) Financial Services and Communications Company :bananadance::goodjob: :hadouken: Now we just need to find a way to get them a smartphone :partysaurus::tophat: (edited)

**mike**
would very much like to do that, maybe come up with packaging which takes a lot less time to assemble, lower cost. though makerbeam is cool...
that's been intent, have stationary nodes with storage, and open source modular mobile with mesh networking, which can achieve global penetration with secure, encrypted networking.

**synth**
yes, stationary, moving nodes creates a lot of problems
skywire only works because its it designed to run over point-to-point segments and not for "mobile adhoc networking" where people are moving around

**arc-over-water**
Do you have a basic program product release? Is it correct at them moment it is just the wallet?

**mike**
so the routing tables don't update that often?

**synth**
https://github.com/skycoin has a lot of different applications
https://github.com/skycoin/bbs works right now
the routing tables only change on new connection; so you make ~10 connections to a pubkey and if some drop you create new ones. so there is redundancy in the path and transit method. "diversity routing"
where as the direct connections between nodes are supposed to change less frequency, such as not more often than 10 seconds. Ideally never changing. any change to underlying physical connectivity, causes update cascade and is a change to network topology (should be minimized).
Where as connection dropping or routes being or connection established, does not change network topology and has no administrative overhead in bandwidth.
short range, mobile ad hoc routing needs to be handled by another protocol like BATMAN, while fixed infrastructure like WIFI hotspots, fiber between cities, ethernet cables etc is handled by the skywire stuff; so if you enter a coffee shop and connect and are there for 30 minutes, then you are fine; but if you are driving down the street connecting to different hotspot every 5 seconds, its not designed for that and needs another protocol layer for "mobile"

**mike**
so nodes can move if the transmission is not interrupted, like a beam forming antenna could do it as long as the beams can be moved fast enough to not interrupt the communication.

**mike**
so nodes can move if the transmission is not interrupted, like a beam forming antenna could do it as long as the beams can be moved fast enough to not interrupt the communication.
see update, they are ok even if some interruption.
makes sense though, works fine for having like mini cell tower and access points, hand held mobile is another protocol if moving from cell to cell.

**synth**
yes, phased array would be fine; or signal interrupted for second or even if signal goes out every hour for and hour and comes back on
but fundamental changes to network topology are more annoying, because everyone involved in routing across the whole network has to get notified; so you actually have to do the updates peer to peer, over CXO; and eventually network has to be segmented so that each node belongs to one or more routing/subscription domains that are partitioned in a sane way
in the current internet the number of hops between two people can be ~40 or 80 or just some insane number; in skycoin it will be 4 or a max of 7. etc, from house to neighborhood, to city, to city/country and then to destination. It wont appear as 40 physical hops, that can each have their own independent congestion
the advantage of phased array, is that you just throw it on your roof and it can scan for whoever it can connect it; and then can connect to different people or best person, without having to climb up on roof and ajust anything; the beam focus is on software control
i like the BBS and VPN, because we do not need to build a physical new internet to run them; we can just tunnel over the existing internet and its useful. It will take years before we see a hardware alternative to the existing internet. Even people are installing 100,000 nodes a month and its growing at 1% per day, it would still take 10 or 15 years until it could replace the existing internet.
There is just so much equipment installed and even if growth rate is massive, it will take forever.

**mike**
yes, this is what i like about it, much easier for automated set-up than pointing antennas, even with motorized directional. had thought of using low frequency for nodes to transmit gps coordinates to locate each other, then point highest possible frequency for range to connect at each other.

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
marathon session today.

**michaelthecryptoguy**
I sure can. As long as jarunik hasn't already started. (edited)

**mike**
Thank you very much for joining us synth, please stop by again.
I will also be continuing to check in on skycoin slack for updates as well,
[skycoin.slack.com](https://skycoin.slack.com)
The closer the integration of Skycoin with Ark, the better.
