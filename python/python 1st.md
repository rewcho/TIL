# 0강. 생기초지식
- 파이선은 다른 언어와 달리 들여쓰기가 중요하다. 동일 레벨인 경우에 들여쓰기가 되지 않으면 에러가 뜬다. 다른 언어로는 들여쓰기로 에러가 나진 않으나 다른 개발자들과 협업을 위해 들여쓰기 습관을 가지는 것이 좋다.
- 기본적으로 변수의 형태는 `[valuename]`으로 표기하며 함수는 `[valuename](수치)`로 표현된다.
- `print(출력 내용 [, sep=구분자] [, end = 끝문자])`로 출력한다. 여기서 sep는 다른 value를 구분하기 위한 것을 의미하며, end는 끝에 붙이는 문자를 의미한다.
- `변수 = input('질문내용')`의 형태로 들어간다.
- 문자열과 수치는 서로 다르게 인식되며, 수치도 정수와 실수, 복소수로 따로 구별된다. 컴퓨터는 수치만을 인식하기 때문에 문자열로 기록된 숫자의 경우 수치로 반드시 변환해야 인식이 되기 때문에 필히 확인하여야 한다.

```
ex)
price = input('가격을 입력하세요 : ')
num = input('수량을 입력하세요 : ')
sum - int(price) * int(num)
print('총액은', sum, '원 입니다.')

가격을 입력하세요 : 500
수량을 입력하세요 : 10
총액은 5000원입니다.
```

# 1강. 변수
- **변수**란 값을 저장하고 있는 메모리에 대한 명칭을 의미한다
- 알파벳, 밑줄, 숫자 등으로 구성된다
- 첫 글짜로 숫자는 사용 불가하다
- 대소문자를 구분하고, 키워드는 사용 불가한다. 주로 변하지 않는 고정값이나 상수는 대문자로 기입하고, 변수에 해당하는 것은 소문자로 기입한다.
- 선언되지 않은 변수 또는 삭제된 변수를 읽으면 예외가 발생한다.

# 2강. 타입
- 0강에서 언급한 문자열과 수치는 서로 다른 타입이기 때문에 서로 호환이 되지 않으며 이용하기 위해서는 해당 타입으로 바꿔줘야 한다. 수치형 타입에는 크게 정수, 실수 복소수 타입이 있다.
## 정수형
- 크기에 제한이 없으면, 값에 따라 크기가 자동 조정이 된다.
- 정수형은 진법에 따라 표기가 되며, 크게 16진법, 8진법, 2진법 등이 있다.
- 다른 타입을 정수형으로 변환할 때는 `int(변수명)` 명령어를 이용한다. 진법을 이용해서 표기할 때에는 `int(변수명, 진법)`으로 표기한다.
| 진법 | 접두 | 사용 가능한 숫자 | 예 |
| --- | ---- | ---- | ---------------- |
| 16진법 | 0x | 0~9, a~f | 0x2f |
| 8진법 | 0o | 0~7 | 0o17 |
| 2진법 | 0b | 1, 1 | 0b1101 |




## 실수형
- 실수형은 소수점 아래도 표현되는 형태로, 실수형으로 타입을 바꾸기 위해서는 `float(변수명)`을 사용한다. 반올림을 할 때에는 `round(변수명 [, 반올림 자리수])`를 사용한다.

## 복소수형
- 복소수형을 표기할 때는 "실수부 + 허수부j" 형태로 표현하며, 복소수 타입으로 바꾸기 위해서는 `complex(변수명)`을 사용한다.
- 주로 과학계가 아니면 잘 사용하지 않는 명령어이다.

## 문자열
- 문자열은 큰 따옴표(")와 작은 따옴표(')로 묶을 수 있으며, 반드시 한 줄로 표현해아 한다.

- 만약 여러 줄로 표기하기 위해서는 삼중 따옴표(""")를 이용해서 표기한다.

- 이 때 여는 따옴표와 닫는 따옴표는 동일해야 한다.

- 따옴표 안에 동일한 따옴표는 사용하지 못하며 에러가 난다. 왜냐하면 안에서 여는 따옴표를 밖의 닫는 따옴표로 인식하기 때문이다. 따라서 따옴표를 서로 구분해줘야 한다.

- 문자열의 경우 표기할 때 다양한 기호를 표기할 수 있다.

- 수치를 문자열로 변경할 경우 `str(변수명)`을 사용한다.

  | 확장열 | 설명        |
  | ------ | ----------- |
  | \n     | 개행        |
  | \t     | 탭          |
  | \"     | 큰 따옴표   |
  | \'     | 작은 따옴표 |
  | \\     | \문자       |


``` ex)
a = "I say \"Hello\" to you"
print(a)
b = ' I say \'Hello\' to you'
print(b)

I say "Hello" to you
I say 'Hello' to you
---------------------------
a = 'first\nsecond'
print(a)

first
second
```

- 본래 수치는 한 줄로 표기하여야 하는데, 편의상 여러줄로 기재할 경우 줄 끝부분에 `\`를 반드시 표기해야 에러가 안 난다.
- 본래 컴퓨터는 수치만 인식하므로, 문자를 인식하기 위해서는 수치와 대응을 이루어야 한다. 그 수치를 확인하기 위해서는 `ord(a)`명령어를 사용하고, 반대로 수치를 통해 해당 문자열로 출력하기 위해서는 `chr(97)`의 명령어를 사용한다.
- 여러개를 나열하고 싶을 때는 `range(ord(A), ord(Z)+1)`로 기입해야 한다. 여기서 맨 끝은 출력이 되지 않기 때문에 끝도 출력하기 위해서는 +1 해줘야 한다.

## 진위형(부울린)
- 진위형은 TRUE, FALSE 두 가지 값만 가지며, 진위를 가릴 때 사용하게 된다.
- 진위형은 비교형이기 때문에, 비교해서 같음을 의미할 때는 =가 아니다 `==`를 사용해야 한다.

## None
 - 어떠한 값도 없음을 나타내는 타입이다.

 ## 컬렉션
 - 여러 값을 묶은 타입을 컬렉션이라 하며, list, tuple, dic이 대표적인 컬렉션 타입이다.
 - list는 해당 데이터를 변환시킬 수 있으며, tuple는 그냥 읽기만 한다.


# 3강. 연산자
## 대입 연산자
- 대입 연산자란 어떠한 값을 변수에 저장하는 것을 의미한다
- 직접 값을 지정해야 한다
- 연산의 결과를 값으로 사용한다
- 사용하지 않는 변수를 읽으면 예외가 발생한다.

## 산술 연산자
- 수치에 사칙연산을 이용해서 표기하는 것이다.

  | 연산자 | 의미        |
  | ------ | ----------- |
  | +      | 더하기      |
  | -      | 빼기        |
  | *      | 곱하기      |
  | /      | 나누기      |
  | **     | 거듭 제곱   |
  | //     | 정수 나누기 |
  | %      | 나머지      |


  


- /는 정수를 실수로 바꾸는 독특한 연산자이기 때문에, 정수만을 다룰 때에는 //를 이용한다. //을 사용하면 몫만이 표기된다.

## 복합 대입 연산자
- 변수의 반복 사용을 줄여주는 연산자이다.
- `a += 1`은 a=a+1을 의미한다.

## 문자열 열산자
- 문자열끼리 `+`를 이용할 경우 그냥 문자열이 연결이 된다.
- 문자열끼리 `*`를 이용할 경우 뒷 수치만큼 해당 문자열이 반복된다.

# 4강. 조건문
## if 조건문
- if 조건문은 단일 라인 표현식이며 표기는 `if 조건 : 명령`으로 표현이 된다
```age = int(input("나이를 입력하세요 : "))
if age < 19:
    print("애들은 가라")

나이를 입력하세요 : 15
애들은 가라
```

- 여기서 조건문을 입력하면 하위 줄은 들여쓰기가 되어서 if 조건문에 종속하게 되며, 만약 들여쓰기가 아니면 if 조건문과 독립적이기에 if 조건문에 해당하지 않게 된다.

- 비교 연산자

  | 연산자 | 설명                        |
  | ------ | --------------------------- |
  | ==     | 같다                        |
  | !=     | 다르다                      |
  | <      | 좌변이 우변보다 작다        |
  | >      | 좌변이 우변보다 크다        |
  | <=     | 좌변이 우변보다 작거나 같다 |
  | >=     | 좌변이 우변보다 크거나 같다 |

  


- 여기서 문자를 적을경우 각 문자마다 컴퓨터가 인식하는 수치로 봐서 서로의 크기를 결정한다. 예를 들어 c와 C 중에 대문자 C가 더 앞서열에 해당하기 때문에 C < c 로 인식이 되며 a와 b는 b가 뒷서열이기 때문에 a < b로 인식한다.

- if에는 거짓 값이 있으며, False, None, 0, ""(비어있는 문자열), [](비어있는 리스트 컬렉션), ()(비어있는 튜블 컬렉션) 등이 있다.

- 논리 연산자

  | 연산자 | 설명                   |
  | ------ | ---------------------- |
  | and    | 두 조건이 모두 참      |
  | or     | 두 조건 중 하나라도 참 |
  | not    | 조건을 반대로 뒤집는다 |

  


- 파이썬의 경우 and형 조건의 경우 한 줄로 기입할 수 있다. 예를 들어, 1 < a < 10을 다른 언어에서는 "a>1 and a<10"으로 표기해야 하는데 파이썬은 "1 < a < 10"으로 표현이 가능하다.
- if 문이 여러 줄인 경우 모두 들여쓰기를 해야 하는데, 같은 들여쓰기로 된 명령들의 집합을 **블록**이라고 한다. 들여쓰기가 다르면 다른 블록의 명령이다.
- if문에서 조건이 false인 경우 실행할 명령어로 `else`가 있으며, 계속해서 명령어를 내릴 경우 `elif`가 있다. 여기서 `elif`는 파이썬만 사용하고, 다른 언어는 `else if`로 기입하여야 한다.
``` money = 6500
if money >=20000:
   print("탕수육을 먹는다")
elif money >10000:
   print("쟁반 짜자을 먹는다")
elif money >=6000:
   print("짜장면을 먹는다")
else:
   print("단무지를 먹는다")

짬뽕을 먹는다
```
