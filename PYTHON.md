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
