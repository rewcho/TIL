- 표현식이란 최종실행결과가 값을 결정하는 것을 의미한다.
- 동적 ㅇㅇ는 실제파일이 아니라 가상의 주소로 입력받고 그걸 브라우저에 표현하기만 한다. 실제 파일은 정적 ㅇㅇ가 한다.
- 경로에 따라 바뀌는 변수를 **경로 변수**라고 부른다. 보통 polls/urls.py 안에 urlspattern에서 polls/ㅇㅇ 에서의 ㅇㅇ를 의미한다.
- 보통 경로 변수는 ``(꺾쇠 괄호)를 사용한다.
- form을 구성할 때 반드시 토큰값을 집어넣어야 한다.
- pk를 가지고 있으면 sql에서 update, pk가 없으면 sql에서 insert에 해당한다.
- 템플릿은 태그 중 for 태그에서는 counter,counter-, first, last 등을 주로 사용한다. 여기서 first, last는 부울린에 해당한다.
- django를 다룰 때 해당 주석을 써야지 HTML의 <!-- -->를 주석처리 하면 안 된다. 이 주석은 실행은 되나 브라우저에서만 각주로 인식할 뿐이다. 이 때 한줄 처리는 {# #}로 해야 한다.
- 뷰에서도 함수를 기초로한 FBV와 크래스를 기초로한 CBV가 있다. 여기서 클래스를 더 많이 사용하는데, 이유는 함수로 하면 반복작업을 하기 때문이다.'
- FK에서 1:1 또는 1:N으로 설정할 때 쓰고, N:M은 Many to Many로 사용하게 된다.
- 클래스로 정의할 시 앞에 정의된 클래스가 없으면 ''를 이용하여 문자열로 표현해야 된다.
- view에는 크게 genericview가 있으며, generic view에서는 templateview(템플릿을 보기), listview(목록 보기), detailview(상세읽기)
- url에서 상속할 때 from . import ㅇㅇ에서 .은 현재의 패키지를 의미한다.
- 템플릿 연동은 db가 없는 뷰를 사용한다.
- 사이드바의 내용을 더 살리고 싶으면 {{block.super}}를 사용한다.
- "|add |에서 `|`는 기존 모델에 추가하라라는 뜻이다.






cf) http의 경우 요청을 하면 딱 한 번 보내고 딱 한번 문자열을 받는다.
cf2) body의 유무는 메서드가 결정한다.
cf3) http의 상태고드 중 40X의 경우 요청이 잘못되었다는 뜻으로, client에 문제가 있는 것이다. 50X는 서버에 문제가 있는 것이다.
url 포트번호에서 80은 생략 가능.
filter
(모델의 클래스 멤버) __(모델의 연산자)