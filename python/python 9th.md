# 17장
# 스레드
- 프로세스는 하나 또는 2개 이상인 쓰레드가 있는데 각 프로세스 당 메인 스레드가 있고 그 외 멀티 스레드 중에 작업 쓰레드(또는 워킹 쓰레드)가 존재한다.
- 마지막 코드를 실행하거나 리턴값을 만나면 실행 종료
- c+++은 메인 스레드가 종료하면 프로세스가 종료되어 다른 스레드를 강제 종료하나, 다른 언어들은 모든 스레드가 종료해야 프로세스가 종료된다.
- 스레딩모듈을 만들 때 스레드 클래스를 함수를 만들거나 상속을 통해 만들어야 한다. 함수를 사용할 경우 `run()` 매서드를 통해 재정의를 해야 한다.
- 파이선에서 스레드를 import할 때 파일명에 thread를 해서는 안된다. import할 때 working dir를 기준으로 판단하기 때문에 thread module이 아닌 해당 파일을 import하기 때문이다.
- 스레드 당 스택이 1개씩 독립적으로 사용하지만, 전역에 해당하는 것은 모든 스레드가 공유하면서 사용한다.
- 스레드는 운영체제가 유지하기 때문에 함수가 진행되었다고해서 메모리에 사라지지 않는다. 따라서 변수의 모양을 같게 해도 덮어쓰지 않으므로 문제가 없다.
- 스레드 동기화란 각 스레드가 서로에게 영향을 끼치는 것에 대한 것이다.

# 네트워크 프로그래밍
- 네트워크를 연결하기 위해서는 주소와 포트번호가 필요하다.
- 서버 연결이 안 될 경우에는 1. 서버가 기동이 안 되어서 2. 방화벽으로 인해 차단되어서 등이 있다.
- 프로토콜에서 많은 것을 정의해야 한다...(구체적인 것은 좀 더 공부해야겠다..)

# 파일 전송 프로그램(매우 중요!!!!!!!!!!!)
- 소켓도 파일처럼 with를 사용시 close가 될 때 자동으로 닫아준다.
- 먼저 보내는 것은 파일크기에 관한 정보를 보내고, 이후 


- CPU에 따라 인코딩된 숫자의 배열이 다 다르기 때문에 숫자 그대로를 인코딩을 한 하고 공통된 문자열로 바꿔서 전송한 후에 그 문자열을 다시 숫자로 바꿔서 인코딩된 것을 사용하는 방식을 사용해서 전송해야 한다.
- program의 receive는 buffer를 통해 이루어지고, LAN을 통해 receive를 할 때에는 os가 담당한다.
- buffer의 내용을 실제 디바이스에 옮기고 자신을 비우는 것을 flush라고 부르며, 이 때 sendall 명령을 사용해서 명령한다. 다만 명령이 많아서 횟수가 많아 시간이 더 걸릴 수 있다.
- 파일을 전송하거나 받을 때 SOCK_STREAM을 사용하면 read의 양과 receive 양의 차이가 생겨도 상관없다. 왜냐하면 buffer에 들어갈 때 구간을 나누는 것이 아닌 하나의 steam을 통해 내려받기 때문이다. 전에 받았던 file 챕터에도 이런 스트리밍을 통해 받았다.
- 파일을 전송할 때 파일명과 data 내용 모두 같이 보내는 것이 좋은데, 구분을 하지 않으면 단일 data 내용으로 인식한다. 따라서 이를 구분해야하는데, 보통 사전을 이용하는 것이 좋다.
- 그래서 jason(Javascript Object Notation) 방식을 이용하여 데이터를 문자열로 객체정보를 교환할 수 있다.
- pickle의 경우 파이썬만 사용할 수 있는 기능이라 호환이 안 되기 때문에 권장되지 않는다.