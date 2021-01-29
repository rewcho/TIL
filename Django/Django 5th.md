- 1:N 에서 FK를 배정할 때에는 N쪽에다 잡는다.
- owner의 경우 데이터에서는 integer로 보지만 Django에서는 유저의 인스턴스로 이해한다. 따라서 신원을 확인할 때에는 접미어로 .id나 .username을 붙이면 확인할 수 있다.
- 모델이 변경되어 컬럼이 추가가 되면 migration이 반드시 필요하다. 단순 메서드 추가라면 migration 없이도 반영이 된다.
- blog/views에서 유효성 검사를 성공했을 때 리턴값인 from_valid(form)은 모델 save()를 호출하는 것이고, success_url로 리다이렉트도 해준다.
```
 def form_valid(self, form):
 form.instance.owner = self.request.user
 return super().form_valid(form)
 ```
- django에서 `LoginRequiredMixin`은 로그인을 한 사람만 해당 게시물에 접근이 가능하게끔 해주는 클래스이다.
- 소유자에게만 수정인 삭제 권한을 주는 클래스는 `OwnerOnlyMixin`에 해당한다.
- OwnerOnlyMixin에서 가장 중요한 것이 모델 인스턴스 얻기와 소유지인지 확인하는 것이다.
- create에 따로 form을 만들지 않았더라도 field와 initial을 지정을 하면 자동으로 만들어준다.
- form_valid에서 수정이나 추가사항이 반영된다.
```
tinymce.init({
 selector:'textarea',
 menubar: false,
 statusbar: false,
 toolbar1:
 ```
- 여기에서 selector는 CSS 선택자에 해당한다.
- fk를 지정할 때 생기는 테이블로 (모델명)_set을 형성하는데, 이 모델명이 길어서 간단한 것으로 바꿔줘야 할 필요성이 생긴다. 이 때 쓰는 명령어가 `related_name="(바꾸는 이름)"`으로 하면 된다.
- 업로드 파일명은 랜덤하게 정해지고, 사용자에게 줘야 할 원본 파일이름 둘 다 관리를 해야 한다.
- entype가 urlencoded나 json의 경우는 text파일을 다루기 때문에 binary와 같은 파일을 전송하기가 어려워진다. 따라서 바이너리 데이터를 전송할 때는 multipart/form-data로 해야 한다.
- 실제 업로드된 파일은 self.request.FILES에 여러 개의 업로드 파일 정보를 관리한다.
- 참고로 self.request.GET은 query 사전을 관리한다.
- self.request.POST는 body 사전을 관리한다.

*args : 가변인수(튜플)
**kwargs : 키워드 가변인수(사전)
fk을 배정하게 되면 pk에 관한 테이블이 생성된다.