- 자식에 관해서 대책가능한 영역을 **블럭**이라고 한다.
- 자식 템플릿은 부모를 상속받아 정의한다.
- 부모 템플릿에서 base는 app과 무관한 것인 공통을 다루고, base_book은 app별로 특화된 것을 공통으로 한다.
- 디렉토리는 다르면서 동일한 이름의 템플릿이 있을 수 있는데, 먼저 읽히는 템플릿이 먼저 적용된다.
- 기존의 블록을 살리고 싶으면 {{block.super}}를 사용한다.
- listview template name : 모델명(소문자)_list
- detailview template name : 모델명(소문자)_detail
- forloop.last는 자동으로 돌아가는 루프변수로 마지막 돌 때 행동을 하라는 명령어이다.
- {% %} 같은 괄호는 파이썬을 기초로 한 것이기 때문에, html로 표현했다고 하더라도 줄이나 탭간격을 지켜야 한다.
- 뷰를 설정할 때 모델과의 연관성을 따져야 한다. 모델과 연관성이 없으면 보다 상위(?)뷰인 템플릿 뷰를 사용하는 것이 좋다.


    def get_context_data(self, **kwargs):
        context = super().get_context_data(**kwargs)
        context['app_list'] = ['polls', 'books']
        return context

위의 함수로 object의 이름을 변경할 수 있다.


    def get_queryset(self):
        """Return the last five published questions."""
        return Question.objects.order_by('pub_date')[:5]



object=self.model.objects.get(pk)
context variable
listview > object.list

경로변수


- static은 실제 다루는 파일
- MEDIA는 파일업로드용 url에 해당한다.
- __init__.py는 패키지라는 뜻
- 설치된 앱을 적용할 때 그냥 앱명을 써도 되지만 해당 앱의 config로 써도 된다.
- admin을 지정할 때 함수를 써도 되지만 데코레이션(@)을 사용해도 된다.
- 다만 함수를 쓸 때는 전체를 지정하게 되지만 특정한 활동을 할 수 없기 때문에 데코레이션으로 더 세부명령을 내릴 수 있게 된다.
- ORM은 database의 종류와 무관하게 적용되어야 한다.
```
create_dt = models.DateTimeField('CREATE DATE', auto_now_add=True)    # insert
modify_dt = models.DateTimeField('MODIFY DATE', auto_now=True)        # update

ordering                                #ListView 디폴트 정렬 기준
 ```

- html 문서에서 {{}} 안에 |가 있으면 이는 필터를 의미한다.
- html 문서에서 ? 오른쪽은 query, 왼쪽은 파일의 경로를 적는다.
- `<a href="?page=ㅇㅇㅇ">`에서 page는 ListView에 해당하기 때문에 반드시 page라고 기재하여야 한다.
- url 인코딩 방식으로 하면 slug로 표현하는 대신 ascii코드문자로만 맵핑을 하여 사용한다.
- 비영어권 문자를 ascii 문자로 변환하는 명령어는 reverse('dd', )이다.
- 즉 http 프로토콜은 ascii 문자 기반 통신이기 때문에, ascii를 utf로 변환하여야 한다.
- 개행문자를 <br>이나 <p>로 바꾸는 것이 {{object|linebreaks}}이다.
- python manage.py runserver 0.0.0.0:8000 으로 적으면 allow host 모두 허용하겠다는 의미이다.