- app install을 나열할 때 관례적으로 기본 앱 -> 서드 파티 앱 -> 기타 앱 으로 순서를 나열한다.
- 같이 허브를 사용할 때 migrate관련 로그파일을 전부 지워야 한다. 0001 initial이라든가 pycache 안에 들어있는 파일을 넣어야 한다.
- 이러한 history 파일을 리셋하기 위해서 명령창에 `python manage.py migrate --fake (앱이름) zero`라고 입력하면 된다.
TaggedObjectLV(태그별 post list 보여주기)
- filter by 는 '='을 이용해서 필터링을 하는 것이고, 그냥 filter __에 관해서 필터링을 하는 것이다.
- self.kwargs에서 kwargs는 경로변수에 해당한다.
- 각 앱당 template에는 해당 앱의 이름을 폴더로 한다.
- formview에서 form의 유효성 검사를 하기 위해서 항목을 추가하는데
```
def form_valid(self, form):
```
식으로 추가한다. 유호성 검사가 통과되었을 때만 이 함수가 호출된다.
- 유효성이 검증된 폼데이터가 저장되어있는 사전을 `form.cleaned_data`이다.
- Q는 보통 query를 뜻한다. 'i'가 들어가면 대소문자를 구분하지 말라는 뜻이다. i는 ignore의 약자이다.
- FormView의 함수에 |는 or란 뜻을 가진다.
- createView는 formview의 상속을 받으며, 내부적으로 insert기능을 한다.
- label을 만들어 input할 수 있게 하는 명령어이다.
```
        <div class="form-group row">
            {{ form.username| add_label_class:"col-form-label col-sm-3 ml-3 font-weight-bold" }}
            <div class="col-sm-5">
                {{ form.username|add_class:"form-control"|attr:"autofocus" }}
            </div>
        </div>
        ```

- form-control은 Bootstrap4에서 정의된 클래스로, width가 100%가 된다.

- view 페이지에서 success url로 redirect해서 들어가게끔 한다.