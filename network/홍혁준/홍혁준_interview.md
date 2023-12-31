## 네트워크 

### 1주차
#### Transport Layer와, Network Layer의 차이에 대해 설명해 주세요.
   > 전송 계층은 패킷을 신뢰성있게 전달되는 지를 보장하는 역할을 하지만 네트워크 계층은 패킷이 어떤 경로로 네트워크를 통해 전달될지를 처리합니다.

#### 각 Layer는 패킷을 어떻게 명칭하나요? 예를 들어, Transport Layer의 경우 Segment라 부릅니다.
   - 응용 (Application Layer): "데이터" 또는 "메시지"
   - 표현 (Presentation Layer): "데이터" 또는 "메시지"
   - 세션 (Session Layer): "데이터" 또는 "메시지"
   - 전송 (Transport Layer): TCP - "세그먼트", UDP - "데이터그램"
   - 네트워크 (Network Layer): "패킷"
   - 데이터 링크 (Data Link Layer): "프레임"
   - 물리 (Physical Layer): "비트"

#### L3 Switch와 Router의 차이에 대해 설명해주세요.
    answer

#### 각 헤더와 Packing Order에 대해 설명해주세요.
    answer

#### ARP에 대해 설명해주세요.
    answer

#### `www.github.com`을 브라우저에 입력하고 엔터를 쳤을 때, 네트워크 상 어떤 일이 일어나는지 최대한 자세하게 설명해주세요.
    answer

#### DNS 쿼리를 통해 얻어진 IP는 어디를 가리키고 있나요?
    answer

#### Web Server와 Web Application Server의 차이에 대해 설명해주세요.
    answer

#### URL, URI, URN은 어떤 차이가 있나요? (Uniform Resource Locator, Uniform Resource Identifier, Uniform Resource Name)
    URL은 자원의 위치를 가리키고. URI는 인터넷 상의 자원을 식별하기 위한 문자열입니다. 즉, 모든 URL은 URI가 되지만 모든 URI가 URL이 될 수는 없습니다.
    URL은 자원의 위치에 영향을 받지 않는 고유 이름을 가리킵니다.

#### DNS에 대해 설명해주세요. (Domain Name System)
    DNS는 도메인 이름을 IP 주소로 변환해주는 시스템입니다.

#### DNS는 몇 계층 프로토콜 인가요?
    answer

#### DNS는 UDP와 TCP 중 어떤 것을 사용하나요?
    answer

#### DNS Recursive Query, Iterative Query가 무엇인가요?
    answer

#### DNS 쿼리 과정에서 손실이 발생하면 어떻게 처리하나요?
    answer

#### DNS 레코드 타입 중 A, CNAME, AAAA의 차이에 대해 설명해주세요.
    answer

#### hosts 파일은 어떤 역할을 하나요? DNS와 비교했을 때 어떤 것이 우선순위가 높나요?
    answer

#### TCP와 UDP 차이에 대해 설명 해주세요.
    TCP는 연결형 서비스로 혼잡, 흐름, 오류 제어 기능을 제공하여 신뢰성있는 데이터 통신을 지원합니다. 
    반면 UDP는 연결형이 아닌 서비스로 간단한 전송 기능만을 제공하고 신뢰성을 보장하지 못합니다.  

#### 왜 HTTP는 TCP를 사용하나요?
   > HTTP는 웹 서버와 클라이언트 간에 정보를 주고받는 프로토콜인데 전송된 데이터의 무결성과 신뢰성이 중요하기 때문에 TCP를 사용합니다.

#### 왜 HTTP/3에서는 UDP(QUIC)를 사용하나요? UDP의 문제가 해결되었나요?
   > answer

#### 본인이 새로운 통신 프로토콜을 TCP나 UDP를 사용해서 구현한다고 하면, 어떤 기준으로 프로토콜을 선택할 것인가요?
   > 개발하려는 애플리케이션의 특성과 필요성에 따라 선택할 것 같습니다. 예를 들어, 신뢰성과 데이터의 순서 보장이 중요하다면 TCP를 선택하고 
   > 신속한 데이터 전달과 실시간성이 중요하다면 UDP를 사용할 것 같습니다.

#### Checksum이 무엇인가요? 그리고 TCP와 UDP 중 어느 프로토콜이 체크섬을 수행하나요?
   > 체크섬은 데이터 패킷의 일부분을 더해서 만든 결과로 수신 측에서 다시 계산해 보낸 측의 체크섬과 비교함으로써 
   > 데이터의 무결성을 확인하고 오류를 검출하는 방법으로 단순하면서 효과적입니다.

#### Checksum을 통해 오류를 정정할 수 있나요?
   > 두 프로토콜 모두 수행합니다.

#### TCP가 신뢰성을 보장할 수 있는 방법에 대해 설명해주세요.
   > ACK를 통해 데이터 수신을 확인하며 이를 통해 패킷 손실이 발생하면 재전송을 요청합니다. 또한 순서 번호를 통해 패킷의 순서도 보장합니다.

#### TCP의 혼잡 제어 처리 방법에 대해 설명해주세요.
   > TCP는 네트워크의 혼잡상황을 감지하고 대응하기 위해 다양한 알고리즘을 사용하는데, 이 알고리즘들은 네트워크 혼잡을 피하기 위해 데이터 전송 속도를 조절하고
   > 패킷 손실 발생 시 빠르게 재전송을 진행합니다.

#### 3-Way Handshaking에 대해 설명해주세요.
   > answer

#### 4-Way Handshaking에 대해 설명해주세요.
   > answer

#### ACK, SYN 같은 정보는 어떻게 전달하는 것인가요?
   > answer

#### 2-Way Handshaking을 하지 않는 이유는 무엇일까요?
   > answer

#### 두 호스트가 동시에 연결을 시도하면, 연결이 가능한가요? 가능하다면 어떻게 통신 연결을 수행하나요?
   > answer

#### SYN Flooding에 대해 설명해주세요.
   > answer

#### TCP 연결 과정에서 3-Way와 4-Way 단계 차이가 나는 이유를 설명해주세요.
   > 클라이언트가 데이터 전송을 마쳤다고 해도 서버는 아직 보낼 데이터가 남아 있을 수 있기 때문에 일단 ACK 패킷만 보내고 데이터를 모두 전송한 후에 자신도 FIN 패킷을 보내기 때문입니다.

#### Server에서 FIN 플래그를 전송하기 전에 전송한 패킷이 라우팅 지연이나 패킷 유실로 인한 재전송 등으로 FIN 패킷보다 늦게 도착한 상황이 발생하면 어떻게 될까요?
   > 해당 현상을 대비해 클라이언트는 서버로부터 FIN 플래그를 수신해도 일정 기간(Time Wait) 동안 세션을 남겨두고 잉여 패킷을 기다리는 과정을 거칩니다.  

#### 초기 Sequence Number인 ISM을 0부터 시작하지 않고 난수를 생성해서 설정하는 이유가 있나요?
   > `Connection을 맺을 때 사용하는 포트는 시간이 지남에 따라 재사용 됩니다. 따라서 두 통신이 과거에 사용된 포트 번호 쌍을 사용할 가능성이 생기고 난수가 아닌 순차적 Number가 전송된다면 이전 커넥션으로부터 오는 패킷으로 인식할 가능성이 있기 때문입니다.

[참조]
- https://velog.io/@backtony/%EB%A9%B4%EC%A0%91-%EC%8B%9C%EB%A6%AC%EC%A6%884-Network
- https://github.com/VSFe/Tech-Interview/blob/main/03-NETWORK.md
