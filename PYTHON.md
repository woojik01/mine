# 파이썬 문법 정리
## 출력
```python
print("안녕하세요")
```
> 안녕하세요
---
## 주석
```python
# 이렇게 하면 코드 취급당하지 않는다.
```
---
## 변수
```python
a = 10
print(a) # a에 저장된, 즉, 10 출력.
```
> 10
---
## 자료형(형변환)
```python
print(int(1)) # 정수
print(float(0.5)) # 실수
print(str("문자")) # 문자
print(bool(True)) # 불리언(참(True) 또는 거짓(False))
```
> 1
> 0.5
> 문자
> True
---
## 연산자
### 산술 연산자
```python
a = 4
b = 2
print(a + b) # 덧셈
print(a - b) # 뺄셈
print(a * b) # 곱셈
print(a ** b) # 거듭제곱
print(a / b) # 나눗셈
print(a // b) # 나눗셈의 몫 구하기
print(a % b) # 나눗셈의 나머지 구하기
```
> 6
> 2
> 8
> 16
> 2
> 2
> 0
---
### 비교 연산자
```python
a == 0 # a가 0과 같다.
a != 0 # a가 0과 같지 않다.
a > 0 # a가 0보다 크다.
a < 0 # a가 0보다 작다.
a >= 0 # a가 0보다 크거나 같다.
a <= 0 # a가 0보다 작거나 같다.
```
---
### 논리 연산자
```python
a = 3
b = 5
a < b and a == b # 'and'는 둘 다 참이여야 True(참)가 된다. 따라서 이 코드는 False(거짓)이다.
a < b or a == b # 'or'은 둘 중 하나만 참이면 True가 된다. 따라서 이 코드는 True이다.
not a < b # 'not'은 결과값을 반전시킨다. 이 코드에서 a < b는 True가 되지만 결과가 반전되어 최종적으로 False가 된다.
```
---
### 대입 연산자
```python
a = 6
a += 2 # a = a + 2
a -= 2 # a = a - 2
a *= 2 # a = a * 2
a **= 2 # a = a ** 2
a /= 2 # a = a / 2
a //= 2 # a = a // 2
a %= 2 # a = a % 2
```
---
### 멤버십 연산자
```python
'a' in 'apple' # True
'b' not in 'apple' # True
```
---
### 식별 연산자
```plain text
추후 주가 예정
```
---
### 비트 연산자
```plain text
추후 추가 예정
```
---
## 입력
```python
name = input("이름: ") # input()은 기본적으로 문자임.
age = int(input("나이: ")) # 문자를 정수로 변환
height = float(input("키: ")) # 문자를 실수로 변환
```
---
## 조건문
```python
a = int(input("a = "))
b = int(input("b = "))
if a < b: # 이때, 꼭 ':'이 마지막에 들어가야 한다.
    print("a가 b보다 더 작다.")
elif a == b:
    print("a와 b가 같다.")
else:
    print("a가 b보다 크다.")
```
> a = 4
> b = 2
> a가 b보다 크다.
---
## 반복문
### for
```python
time = int(input("횟수: "))
for i in range(time):
    print(time)
    time -= 1
```
> 횟수: 3
> 3
> 2
> 1
---
### while
```python
q = str("None")
while q != "quit":
    q = input("끝?: ")
    if q == "stop":
        print("드디어 끝났다.")
        break # 반복을 깬다.
    elif q == "skip":
        pass # 아무것도 하지 않음
    elif q != "quit"
        print("아니구나...")
        continue # 반복을 다시 처음부터 한다.
```
> 끝?: no
> 아니구나...
> 끝?: quit
---
## 문자열
### 인덱싱
```python
text = "hello"
print(text[0]) # 첫 번째 문자는 0임.
print(text[1]) # 두 번째 문자는 1임.
```
> h
> e
---
### 슬라이싱
```python
text = "hello"
print(text[0:2])
print(text[2:5])
'''
⭐️중요: 단, 시작은 포함, 끝은 비포함
'''
```
> he
> llo
---
### 문자열 메서드
### split()
```python
text = "사과, 바나나, 포도"
print(text.split(", "))
```
> ['사과', '바나나', '포도']
---
### replace()
```python
text = "I like Java"
print(text.replace("Java", "Python"))
```
> I like Python
---
### strip()
```python
name = input("이름: ").strip()
print()
```
