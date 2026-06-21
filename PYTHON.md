# 파이썬 문법 정리

## 출력

`print()`를 사용하여 값을 출력할 수 있다.

```python
print("안녕하세요")
```

출력 결과:

```text
안녕하세요
```

---

## 주석

주석은 코드 실행에 영향을 주지 않으며, 설명을 작성할 때 사용한다.

```python
# 이렇게 작성한 내용은 실행되지 않는다.
```

---

## 변수

변수는 데이터를 저장하는 공간이다.

```python
a = 10
print(a)
```

출력 결과:

```text
10
```

---

## 자료형

파이썬의 기본 자료형은 다음과 같다.

```python
a = 10        # int (정수)
b = 3.14      # float (실수)
c = "문자"    # str (문자열)
d = True      # bool (불리언)
```

---

## 형변환

자료형을 다른 자료형으로 변환할 수 있다.

```python
print(int(1.5))
print(float(1))
print(str(100))
print(bool(True))
```

출력 결과:

```text
1
1.0
100
True
```

---

## 연산자

### 산술 연산자

```python
a = 4
b = 2

print(a + b)   # 덧셈
print(a - b)   # 뺄셈
print(a * b)   # 곱셈
print(a ** b)  # 거듭제곱
print(a / b)   # 나눗셈
print(a // b)  # 몫
print(a % b)   # 나머지
```

출력 결과:

```text
6
2
8
16
2.0
2
0
```

---

### 비교 연산자

```python
a == 0   # 같다
a != 0   # 같지 않다
a > 0    # 크다
a < 0    # 작다
a >= 0   # 크거나 같다
a <= 0   # 작거나 같다
```

---

### 논리 연산자

```python
a = 3
b = 5

print(a < b and a == b)
print(a < b or a == b)
print(not a < b)
```

출력 결과:

```text
False
True
False
```

#### and

두 조건이 모두 참일 때 `True`

#### or

둘 중 하나만 참이어도 `True`

#### not

결과를 반대로 바꾼다.

---

### 대입 연산자

```python
a = 6

a += 2
a -= 2
a *= 2
a **= 2
a /= 2
a //= 2
a %= 2
```

각각 다음과 같다.

```python
a += 2  # a = a + 2
a -= 2  # a = a - 2
a *= 2  # a = a * 2
a **= 2 # a = a ** 2
a /= 2  # a = a / 2
a //= 2 # a = a // 2
a %= 2  # a = a % 2
```

---

### 멤버십 연산자

```python
'a' in 'apple'
'b' not in 'apple'
```

출력 결과:

```text
True
True
```

---

### 식별 연산자

`is`는 값이 아니라 객체가 같은지를 비교한다.

```python
a = [1, 2, 3]
b = a
c = [1, 2, 3]

print(a is b)
print(a is c)
print(a is not c)
```

출력 결과:

```text
True
False
True
```

---

### 비트 연산자

```python
a = 5
b = 3

print(a & b)
print(a | b)
print(a ^ b)
print(~a)
```

출력 결과:

```text
1
7
6
-6
```

---

## 입력

`input()`은 기본적으로 문자열(str)을 반환한다.

```python
name = input("이름: ")
age = int(input("나이: "))
height = float(input("키: "))
```

---

## 조건문

```python
a = int(input("a = "))
b = int(input("b = "))

if a < b:
    print("a가 b보다 더 작다.")
elif a == b:
    print("a와 b가 같다.")
else:
    print("a가 b보다 크다.")
```

실행 예시:

```text
a = 4
b = 2
a가 b보다 크다.
```

---

## 반복문

### for

`range(n)`은 0부터 n-1까지 반복한다.

```python
for i in range(3):
    print(i)
```

출력 결과:

```text
0
1
2
```

역순 반복:

```python
for i in range(3, 0, -1):
    print(i)
```

출력 결과:

```text
3
2
1
```

---

### while

조건이 참인 동안 반복한다.

```python
q = "None"

while q != "quit":
    q = input("끝?: ")

    if q == "stop":
        print("드디어 끝났다.")
        break

    elif q == "skip":
        pass

    elif q != "quit":
        print("아니구나...")
        continue
```

실행 예시:

```text
끝?: no
아니구나...
끝?: quit
```

#### break

반복문을 즉시 종료한다.

#### continue

현재 반복을 건너뛰고 다음 반복으로 넘어간다.

#### pass

아무 동작도 수행하지 않는다.

---

## 문자열

### 인덱싱

문자열의 첫 번째 위치는 0이다.

```python
text = "hello"

print(text[0])
print(text[1])
```

출력 결과:

```text
h
e
```

---

### 슬라이싱

```python
text = "hello"

print(text[0:2])
print(text[2:5])
```

출력 결과:

```text
he
llo
```

⭐️ 시작 위치는 포함하고 끝 위치는 포함하지 않는다.

---

## 문자열 메서드

### split()

```python
text = "사과, 바나나, 포도"

print(text.split(", "))
```

출력 결과:

```text
['사과', '바나나', '포도']
```

---

### replace()

```python
text = "I like Java"

print(text.replace("Java", "Python"))
```

출력 결과:

```text
I like Python
```

---

### strip()

```python
name = input("이름: ").strip()

print(f"안녕하세요, {name} 님.")
```

---

### find()

```python
text = "hello"

print(text.find("e"))
print(text.find("x"))
```

출력 결과:

```text
1
-1
```

문자가 없으면 `-1`을 반환한다.

---

### count()

```python
text = "hello"

print(text.count("l"))
```

출력 결과:

```text
2
```

---

### join()

```python
words = ["사과", "바나나", "포도"]

print(",".join(words))
print(" ".join(words))
```

출력 결과:

```text
사과,바나나,포도
사과 바나나 포도
```

⭐️ `"구분자".join(리스트)` 형태로 사용한다.

---

### upper(), lower()

```python
text = "Hello"

print(text.upper())
print(text.lower())
```

출력 결과:

```text
HELLO
hello
```

---

### 기타 문자열 메서드

```python
text = "hello"

print(text.startswith("he"))
print(text.endswith("lo"))
```

출력 결과:

```text
True
True
```

## 리스트

리스트(list)는 여러 값을 순서대로 저장하는 자료형이다.

```python
fruits = ["사과", "바나나", "포도"]

print(fruits)
```

출력 결과:

```text
['사과', '바나나', '포도']
```

---

### 인덱싱

```python
fruits = ["사과", "바나나", "포도"]

print(fruits[0])
print(fruits[1])
```

출력 결과:

```text
사과
바나나
```

---

### 슬라이싱

```python
fruits = ["사과", "바나나", "포도", "딸기"]

print(fruits[1:3])
```

출력 결과:

```text
['바나나', '포도']
```

⭐️ 시작 위치는 포함하고 끝 위치는 포함하지 않는다.

---

### append()

리스트의 맨 뒤에 요소를 추가한다.

```python
fruits = ["사과", "바나나"]

fruits.append("포도")

print(fruits)
```

출력 결과:

```text
['사과', '바나나', '포도']
```

---

### insert()

원하는 위치에 요소를 삽입한다.

```python
fruits = ["사과", "포도"]

fruits.insert(1, "바나나")

print(fruits)
```

출력 결과:

```text
['사과', '바나나', '포도']
```

---

### remove()

특정 값을 삭제한다.

```python
fruits = ["사과", "바나나", "포도"]

fruits.remove("바나나")

print(fruits)
```

출력 결과:

```text
['사과', '포도']
```

---

### pop()

특정 위치의 요소를 꺼내면서 삭제한다.

```python
fruits = ["사과", "바나나", "포도"]

print(fruits.pop())
print(fruits)
```

출력 결과:

```text
포도
['사과', '바나나']
```

---

### sort()

리스트를 정렬한다.

```python
numbers = [3, 1, 4, 2]

numbers.sort()

print(numbers)
```

출력 결과:

```text
[1, 2, 3, 4]
```

---

### reverse()

리스트의 순서를 뒤집는다.

```python
numbers = [1, 2, 3, 4]

numbers.reverse()

print(numbers)
```

출력 결과:

```text
[4, 3, 2, 1]
```

---

### len()

리스트의 길이를 구한다.

```python
fruits = ["사과", "바나나", "포도"]

print(len(fruits))
```

출력 결과:

```text
3
```

---

## 튜플

튜플(tuple)은 여러 값을 저장할 수 있지만, 값을 수정할 수 없는 자료형이다.

```python
numbers = (1, 2, 3)

print(numbers)
```

출력 결과:

```text
(1, 2, 3)
```

---

### 인덱싱

```python
numbers = (10, 20, 30)

print(numbers[0])
```

출력 결과:

```text
10
```

---

### 슬라이싱

```python
numbers = (10, 20, 30, 40)

print(numbers[1:3])
```

출력 결과:

```text
(20, 30)
```

---

### count()

특정 값의 개수를 구한다.

```python
numbers = (1, 2, 2, 3)

print(numbers.count(2))
```

출력 결과:

```text
2
```

---

### index()

특정 값의 위치를 구한다.

```python
numbers = (10, 20, 30)

print(numbers.index(20))
```

출력 결과:

```text
1
```

---

## 딕셔너리

딕셔너리(dictionary)는 `키(key): 값(value)` 형태로 데이터를 저장하는 자료형이다.

```python
person = {
    "name": "Alice",
    "age": 20
}

print(person)
```

출력 결과:

```text
{'name': 'Alice', 'age': 20}
```

---

### 값 접근

```python
person = {
    "name": "Alice",
    "age": 20
}

print(person["name"])
```

출력 결과:

```text
Alice
```

---

### 값 추가 및 수정

```python
person = {
    "name": "Alice"
}

person["age"] = 20

print(person)
```

출력 결과:

```text
{'name': 'Alice', 'age': 20}
```

---

### del

키와 값을 삭제한다.

```python
person = {
    "name": "Alice",
    "age": 20
}

del person["age"]

print(person)
```

출력 결과:

```text
{'name': 'Alice'}
```

---

### keys()

모든 키를 반환한다.

```python
person = {
    "name": "Alice",
    "age": 20
}

print(person.keys())
```

출력 결과:

```text
dict_keys(['name', 'age'])
```

---

### values()

모든 값을 반환한다.

```python
person = {
    "name": "Alice",
    "age": 20
}

print(person.values())
```

출력 결과:

```text
dict_values(['Alice', 20])
```

---

### items()

모든 키와 값을 튜플 형태로 반환한다.

```python
person = {
    "name": "Alice",
    "age": 20
}

print(person.items())
```

출력 결과:

```text
dict_items([('name', 'Alice'), ('age', 20)])
```

---

## 집합(set)

집합(set)은 중복을 허용하지 않는 자료형이다.

```python
numbers = {1, 2, 3, 3, 2}

print(numbers)
```

출력 결과:

```text
{1, 2, 3}
```

---

### add()

요소를 추가한다.

```python
numbers = {1, 2, 3}

numbers.add(4)

print(numbers)
```

출력 결과:

```text
{1, 2, 3, 4}
```

---

### remove()

요소를 삭제한다.

```python
numbers = {1, 2, 3}

numbers.remove(2)

print(numbers)
```

출력 결과:

```text
{1, 3}
```

---

### 합집합

```python
a = {1, 2, 3}
b = {3, 4, 5}

print(a | b)
```

출력 결과:

```text
{1, 2, 3, 4, 5}
```

---

### 교집합

```python
a = {1, 2, 3}
b = {3, 4, 5}

print(a & b)
```

출력 결과:

```text
{3}
```

---

### 차집합

```python
a = {1, 2, 3}
b = {3, 4, 5}

print(a - b)
```

출력 결과:

```text
{1, 2}
```

## 함수

함수(function)는 특정 작업을 수행하는 코드를 묶어 재사용할 수 있게 해준다.

```python
def hello():
    print("안녕하세요")
    
hello()
```

출력 결과:

```text
안녕하세요
```

---

### 매개변수(Parameter)

함수에 값을 전달할 수 있다.

```python
def hello(name):
    print(f"안녕하세요, {name} 님.")

hello("Python")
```

출력 결과:

```text
안녕하세요, Python 님.
```

---

### 반환값(return)

함수의 실행 결과를 반환할 수 있다.

```python
def add(a, b):
    return a + b

result = add(3, 5)

print(result)
```

출력 결과:

```text
8
```

---

### 기본값 매개변수

기본값을 지정할 수 있다.

```python
def hello(name="손님"):
    print(f"안녕하세요, {name} 님.")

hello()
hello("Python")
```

출력 결과:

```text
안녕하세요, 손님 님.
안녕하세요, Python 님.
```

---

### 여러 개의 반환값

튜플 형태로 여러 값을 반환할 수 있다.

```python
def calc(a, b):
    return a + b, a - b

x, y = calc(5, 3)

print(x)
print(y)
```

출력 결과:

```text
8
2
```

---

### 가변 위치 인자(*args)

전달받는 인자의 개수가 정해져 있지 않을 때 사용한다.

```python
def total(*args):
    print(args)
    
total(1, 2, 3)
```

출력 결과:

```text
(1, 2, 3)
```

---

### 가변 키워드 인자(**kwargs)

키워드 형태의 인자를 여러 개 받을 수 있다.

```python
def profile(**kwargs):
    print(kwargs)

profile(name="Python", version=3)
```

출력 결과:

```text
{'name': 'Python', 'version': 3}
```

---

## 람다 함수

람다 함수(lambda)는 간단한 함수를 한 줄로 표현할 때 사용한다.

```python
add = lambda a, b: a + b

print(add(3, 5))
```

출력 결과:

```text
8
```

---

## 예외 처리

예외(exception)는 프로그램 실행 중 발생하는 오류를 의미한다.

```python
try:
    print(10 / 0)
except ZeroDivisionError:
    print("0으로 나눌 수 없습니다.")
```

출력 결과:

```text
0으로 나눌 수 없습니다.
```

---

### try

예외가 발생할 수 있는 코드를 작성한다.

```python
try:
    print(int("abc"))
except:
    print("오류 발생")
```

출력 결과:

```text
오류 발생
```

---

### except

발생한 예외를 처리한다.

```python
try:
    num = 10 / 0
except ZeroDivisionError:
    print("0으로 나눌 수 없습니다.")
```

출력 결과:

```text
0으로 나눌 수 없습니다.
```

---

### else

예외가 발생하지 않았을 때 실행된다.

```python
try:
    print(10 / 2)
except ZeroDivisionError:
    print("오류 발생")
else:
    print("정상적으로 실행되었습니다.")
```

출력 결과:

```text
5.0
정상적으로 실행되었습니다.
```

---

### finally

예외 발생 여부와 관계없이 항상 실행된다.

```python
try:
    print(10 / 0)
except ZeroDivisionError:
    print("오류 발생")
finally:
    print("프로그램 종료")
```

출력 결과:

```text
오류 발생
프로그램 종료
```

---

### raise

직접 예외를 발생시킬 수 있다.

```python
age = -1

if age < 0:
    raise ValueError("나이는 음수가 될 수 없습니다.")
```

실행 결과:

```text
ValueError: 나이는 음수가 될 수 없습니다.
```

---

## 파일 입출력

파일을 읽거나 쓸 때는 `open()` 함수를 사용한다.

---

### 파일 쓰기

```python
file = open("example.txt", "w")

file.write("Hello")

file.close()
```

---

### 파일 읽기

```python
file = open("example.txt", "r")

print(file.read())

file.close()
```

출력 결과:

```text
Hello
```

---

### with 문

파일을 자동으로 닫아 주기 때문에 권장되는 방법이다.

```python
with open("example.txt", "w") as file:
    file.write("Hello")

with open("example.txt", "r") as file:
    print(file.read())
```

출력 결과:

```text
Hello
```

---

### readline()

한 줄씩 읽는다.

```python
with open("example.txt", "r") as file:
    print(file.readline())
```

출력 결과:

```text
Hello
```

---

### readlines()

모든 줄을 리스트 형태로 읽는다.

```python
with open("example.txt", "r") as file:
    print(file.readlines())
```

출력 결과:

```text
['Hello']
```

---

### 파일 모드

| 모드     | 설명           |
| ------ | ------------ |
| `"r"`  | 읽기           |
| `"w"`  | 쓰기(기존 내용 삭제) |
| `"a"`  | 이어쓰기         |
| `"x"`  | 새 파일 생성      |
| `"rb"` | 바이너리 읽기      |
| `"wb"` | 바이너리 쓰기      |

---

### 파일 존재 여부 확인

```python
import os

print(os.path.exists("example.txt"))
```

출력 결과:

```text
True
```

## 클래스와 객체

클래스(class)는 객체를 만들기 위한 설계도이며, 객체(object)는 클래스로부터 생성된 인스턴스이다.

```python
class Person:
    pass

person = Person()

print(type(person))
```

출력 결과:

```text
<class '__main__.Person'>
```

---

### 생성자 `__init__()`

객체가 생성될 때 자동으로 호출되는 메서드이다.

```python
class Person:
    def __init__(self, name):
        self.name = name

person = Person("Python")

print(person.name)
```

출력 결과:

```text
Python
```

---

### 메서드

클래스 내부에 정의된 함수를 메서드라고 한다.

```python
class Dog:
    def bark(self):
        print("멍멍")

dog = Dog()

dog.bark()
```

출력 결과:

```text
멍멍
```

---

### 클래스 변수

모든 객체가 공유하는 변수이다.

```python
class Student:
    school = "Python High School"

print(Student.school)
```

출력 결과:

```text
Python High School
```

---

### 인스턴스 변수

객체마다 독립적으로 가지는 변수이다.

```python
class Student:
    def __init__(self, name):
        self.name = name

a = Student("A")
b = Student("B")

print(a.name)
print(b.name)
```

출력 결과:

```text
A
B
```

---

## 상속

기존 클래스의 기능을 물려받아 새로운 클래스를 만들 수 있다.

```python
class Animal:
    def eat(self):
        print("먹는다")

class Dog(Animal):
    pass

dog = Dog()

dog.eat()
```

출력 결과:

```text
먹는다
```

---

### 메서드 오버라이딩

부모 클래스의 메서드를 재정의할 수 있다.

```python
class Animal:
    def sound(self):
        print("소리")

class Dog(Animal):
    def sound(self):
        print("멍멍")

dog = Dog()

dog.sound()
```

출력 결과:

```text
멍멍
```

---

### super()

부모 클래스의 메서드를 호출할 수 있다.

```python
class Animal:
    def __init__(self):
        print("Animal 생성")

class Dog(Animal):
    def __init__(self):
        super().__init__()
        print("Dog 생성")

dog = Dog()
```

출력 결과:

```text
Animal 생성
Dog 생성
```

---

## 모듈

모듈(module)은 함수나 클래스 등을 모아 둔 파이썬 파일이다.

```python
import math

print(math.sqrt(16))
```

출력 결과:

```text
4.0
```

---

### from ... import

특정 요소만 가져올 수 있다.

```python
from math import pi

print(pi)
```

출력 결과:

```text
3.141592653589793
```

---

### 별칭(alias)

`as`를 사용하여 이름을 변경할 수 있다.

```python
import math as m

print(m.factorial(5))
```

출력 결과:

```text
120
```

---

## 패키지

패키지(package)는 여러 모듈을 묶어 놓은 폴더이다.

예시 구조:

```text
my_package
│
├── main.py
├── module1.py
└── module2.py
```

사용 예시:

```python
from my_package import module1
```

---

## 리스트 컴프리헨션

반복문을 이용하여 리스트를 간결하게 생성할 수 있다.

```python
numbers = [x for x in range(5)]

print(numbers)
```

출력 결과:

```text
[0, 1, 2, 3, 4]
```

---

### 조건문 사용

```python
even_numbers = [x for x in range(10) if x % 2 == 0]

print(even_numbers)
```

출력 결과:

```text
[0, 2, 4, 6, 8]
```

---

## 내장 함수

### len()

객체의 길이를 반환한다.

```python
text = "Hello"

print(len(text))
```

출력 결과:

```text
5
```

---

### range()

일정 범위의 숫자를 생성한다.

```python
print(list(range(5)))
```

출력 결과:

```text
[0, 1, 2, 3, 4]
```

---

### sum()

합계를 구한다.

```python
numbers = [1, 2, 3]

print(sum(numbers))
```

출력 결과:

```text
6
```

---

### max()

최댓값을 반환한다.

```python
numbers = [3, 8, 1]

print(max(numbers))
```

출력 결과:

```text
8
```

---

### min()

최솟값을 반환한다.

```python
numbers = [3, 8, 1]

print(min(numbers))
```

출력 결과:

```text
1
```

---

### abs()

절댓값을 반환한다.

```python
print(abs(-10))
```

출력 결과:

```text
10
```

---

### round()

반올림한 값을 반환한다.

```python
print(round(3.14159, 2))
```

출력 결과:

```text
3.14
```

---

### sorted()

정렬된 새로운 객체를 반환한다.

```python
numbers = [3, 1, 4, 2]

print(sorted(numbers))
```

출력 결과:

```text
[1, 2, 3, 4]
```

---

### reversed()

역순 반복 객체를 반환한다.

```python
numbers = [1, 2, 3]

print(list(reversed(numbers)))
```

출력 결과:

```text
[3, 2, 1]
```

---

### enumerate()

인덱스와 값을 함께 반환한다.

```python
fruits = ["사과", "바나나", "포도"]

for index, value in enumerate(fruits):
    print(index, value)
```

출력 결과:

```text
0 사과
1 바나나
2 포도
```

---

### zip()

여러 iterable 객체를 묶어 준다.

```python
a = [1, 2, 3]
b = ["A", "B", "C"]

print(list(zip(a, b)))
```

출력 결과:

```text
[(1, 'A'), (2, 'B'), (3, 'C')]
```

---

### map()

모든 요소에 함수를 적용한다.

```python
numbers = [1, 2, 3]

result = list(map(lambda x: x * 2, numbers))

print(result)
```

출력 결과:

```text
[2, 4, 6]
```

---

### filter()

조건에 맞는 요소만 추출한다.

```python
numbers = [1, 2, 3, 4, 5]

result = list(filter(lambda x: x % 2 == 0, numbers))

print(result)
```

출력 결과:

```text
[2, 4]
```
