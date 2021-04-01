- 회전 시켰을 때 life cycle를 한 번 파괴하고 다시 실행하는 방식으로 운영한다.
- activity stack이 여러개 쌓이면 모두 stop상태로 존재하게 된다.
- back 버튼의 의미는 가장 위에 있는 스택을 날려버리는 행위이다.(보이는 화면을 제거)
- 바로 직전 stack이 resume이 된다.
- activity 사이끼리 서로 정보를 직접 전달하지 못하기 때문에 android os를 거쳐서 정보를 전달한다.
- 이를 극복하기 위한 용도로 사용하는 객체를 intent객체라고 부른다.
- 종료 직전의 상태를 저정하는 매서드는 `savedInstanceState`이다.
- 'inflate' xml(text)로 구현된 것은 실제 객체 인스턴스 생성으로 구체화하는 작업을 말한다.
- 안드로이드의 서비스를 얻을 때 사용하는 매서드로 `getSystemService()`가 있다.
- inflate를 할 때 사용하는 as는 캐스팅을 하기 위한 것이다.