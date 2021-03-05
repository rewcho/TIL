MariaDB : RDMS

여기서 r은 SQL로 표현

mongodb는 document 지향

스키마란 형태를 말함

몽고db는 형태고정을 할 필요가 없다.(no sql)

샤딩 : 1개의 데이터를 서버별로 분할해서 저장하는 것을 말함.

다큐먼트는 sql에서 행과 비슷하고, 데이터 형태는 파이썬의 사전과 유사함.

find 매서드는 sql의 select 매서드와 유사하다.

_id는 sql의 자동으로 생성되는 primary key에 해당.(자동으로 생성)

처음 key를 입력할 때 공백이 없으면 ""를 생략할 수 있다. 그러나 공백이 있거냐 **.**를 통하여 구별할 때에는 ""를 사용하여야 한다.

ObjectId는 uuid이며, 서버에서 발급이 아닌 클라이언트에서 발급

Mongo는 Maria와 다르게 에러가 거의 안 나기 때문에 오타에 주의해야 한다. 대소문자 역시 Mongo에서는 인식하지만 Maria는 인식하지 못한다.

deletemany({})로 하면 전체 삭제이지만 컬렉션은 남아있음
drop은 컬렉션 자체를 삭제

sort매서드는 배열정리하는 매서드. 1이면 오름차순, -1이면 내림차순이다.

insert와 insertOne, insertMany 모두 기능은 같지만 리턴값이 다르다. insert는 노 리턴, one은 1개, many는 기입한 모두 리턴값

findOne은 특정 필드에 대해 검색을 할 때 주로 사용하게 된다.