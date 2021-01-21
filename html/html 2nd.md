- table에서 style은 CSS에 해당하며 상위 탭에 맞춘다.
- 받은 데이터를 구분할 때 경로에 `&`로 표시된다.
- 폼 태그에서 메서드의 경우 get이 default에 해당한다.
- get 방식은 url에 경로가 들어가며, 길이에 한계가 있고, 보안에 매우 쉽게 노출된다.
- 따라서 이를 극복하고자 post를 사용한다.
- 각 타입마다 default 값이 있으며, 이는 브라우저마다 다르다.
- required는 property에 해당하며, 반드시 입력하지 않으면 안된다.
- placeholder는 어디든 들어갈 수 있으나 일단 들어가면 사라진다.
- 여러 줄을 입력할 때에는 textarea를 입력한다.
- 동그라미 선택지는 하나 밖에 선택할 수 없기 때문에 radio라고 부른다.
- radio는 위치와 상관없이 name이 같아야 작동한다.
- 변수(?)와 비슷한 name은 attribute에 해당하고 함수(?)와 비슷한 check는 property에 해당한다.
- input할 텍스트는 입력을 안 했을 때 빈란으로 넘어가나 radio는 입력 안 하면 아예 안 넘어간다. 이와같이 radio를 이용한 선택지는 파이썬에서 사전으로 이용할 수 있다.
- 그런데 기본적으로 문자열이기 때문에 변환과정이 필요하다.
- option은 기능은 radio와 같으나 표현방식이 다르다.
- option에서 multiple을 부여하면 checkbox와 같은 기능을 하면 된다. 이 때 Ctrl+클릭으로 복수지정이 가능하다.

(- 폼 태그에서 value는 실제 입력값에 대응이 된다.)

# html5 추가 기능
## 입력 양식의 주요 property
- readonly : 수정 불가
- disabled : 텍스트 비활성화
- autocomplete : 
- div 태그 : block 형식으로 분할(끝나는 태그를 만나면 줄이 바뀜)
- span 태그 : 인라인(inline) 형식으로 분할(끝나는 태그를 만나도 줄이 안 바뀜)
