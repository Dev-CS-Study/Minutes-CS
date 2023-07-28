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
#### `www.github.com`을 브라우저에 입력하고 엔터를 쳤을 때, 네트워크 상 어떤 일이 일어나는지 최대한 자세하게 설명해주세요.
#### DNS에 대해 설명해주세요.
#### TCP와 UDP 차이에 대해 설명 해주세요.
#### 3-Way Handshake에 대해 설명해주세요.
#### 4-Way Handshake에 대해 설명해주세요.
#### TCP 연결 과정에서 3-Way와 4-Way 단계 차이가 나는 이유를 설명해주세요.
   > 클라이언트가 데이터 전송을 마쳤다고 해도 서버는 아직 보낼 데이터가 남아 있을 수 있기 때문에 일단 ACK 패킷만 보내고 데이터를 모두 전송한 후에 자신도 FIN 패킷을 보내기 때문입니다.
#### Server에서 FIN 플래그를 전송하기 전에 전송한 패킷이 라우팅 지연이나 패킷 유실로 인한 재전송 등으로 FIN 패킷보다 늦게 도착한 상황이 발생하면 어떻게 될까요?
   > 해당 현상을 대비해 클라이언트는 서버로부터 FIN 플래그를 수신해도 일정 기간(Time Wait) 동안 세션을 남겨두고 잉여 패킷을 기다리는 과정을 거칩니다.  
#### 초기 Sequence Number인 ISM을 0부터 시작하지 않고 난수를 생성해서 설정하는 이유가 있나요?
   > `Connection을 맺을 때 사용하는 포트는 시간이 지남에 따라 재사용 됩니다. 따라서 두 통신이 과거에 사용된 포트 번호 쌍을 사용할 가능성이 생기고 난수가 아닌 순차적 Number가 전송된다면 이전 커넥션으로부터 오는 패킷으로 인식할 가능성이 있기 때문입니다.

[참조]
- https://velog.io/@backtony/%EB%A9%B4%EC%A0%91-%EC%8B%9C%EB%A6%AC%EC%A6%884-Network
- https://github.com/VSFe/Tech-Interview/blob/main/03-NETWORK.md
