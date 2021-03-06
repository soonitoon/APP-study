# 1주차: 변수, 타입, 조건문, 함수

[학습 동영상 🎬](https://www.youtube.com/watch?v=cgsJC3Pp5K0&list=PLa7Lj786Q-Gts3-LsBl5I56YQrQb4sHxI&index=4)

> 동영상에 나오는 repl은 예전 버전으로, 현재 버전과 다르게 생긴 부분들은 무시하셔도 됩니다.

## 요약 노트

### 변수

```python
# '#'으로 시작하는 문장은 프로그램이 실행하지 않아요.

# 원하는 이름의 변수에 원하는 값을 저장하세요.
# print()는 변수에 담긴 값을 출력해줍니다.

a = 1
b = 2
c = b - a
d = '안녕'

print(a) # 1
print(b) # 2
print(c) # 1
print(d) # 안녕
```

### 타입

```python
# 변수에 저장할 수 있는 값에는 종류가 있어요.
# 지금은 정수와 문자열 두 종류만 알아봐요.

a = 1 # 정수입니다.
b = '안녕' # 문자열입니다.

# 숫자는 사칙연산을 할 수 있어요.

a = 1 + 2 # 3
b = 2 - 1 # 1
c = 2 * 2 # 4
d = 4 / 2 # 2.0

# 괄호를 사용해 연산의 우선순위를 지정할 수도 있어요.

e = (1 + 2) * 4 # 12

# 더 복잡한 연산도 가능합니다.

# 나누기의 몫만 구하는 연산입니다.

f = 3 // 2 # 1

# 나누기의 나머지만 구하는 연산입니다.

g = 5 % 2 # 1

# 문자열은 '' 혹은 ""로 감싸서 나타냅니다.

hello = '안녕하세요.'
hello2 = "반갑습니다."

# 문자열을 감싸지 않으면 에러가 생겨요.

hello = 안녕하세요
# Traceback (most recent call last):
#  File "<stdin>", line 1, in <module>
# NameError: name '안녕하세요' is not defined

# 문자열도 더하기를 할 수 있어요.

print(hello + hello2) # 안녕하세요.반갑습니다.
print(hello + hello2 + '저는 누구에요.') # 안녕하세요.반갑습니다.저는 누구에요.
```

### 타입 간 연산

```python
# 숫자와 문자열은 연산할 수 없어요.

print('내 나이는' + 21) # 오류 ⛔️

# 대신 숫자를 문자로 바꿔서 더합니다.

print('내 나이는' + str(21)) # 내 나이는21

# str() 안에 들어간 숫자는 문자열이 돼서 나옵니다.

# 반대로 문자를 숫자로 바꿀수도 있어요.

print(21 + '1') # 오류 ⛔️
print(21 + int('1')) # 22
```

### 불리언

```python
# 불리어는 참과 거짓 둘 중 하나만 가질 수 있어요.
# 참은 True, 거짓은 False에요. 앞글자가 대문자인 것에 주의하세요.

isTrue = True
isFalse = False
```

### 조건문

```python
# 특정 조건에 따라 실행하거나 실행하지 않아요.

if 3 > 2:
    print('정답입니다.')

# 만약 3이 2보다 크면 들여쓰기 한 부분을 실행해요.
# 들여쓰기는 tab 키로 해요.

# 다양한 조건의 예시에요 ⬇️

if 3 < 2:
    print('정답입니다.') # 절대 실행되지 않아요 ⛔️

if 3 < 3:
    print('정답입니다.') # 절대 실행되지 않아요 ⛔️

if 3 <= 3:
    print('정답입니다.') # 언제나 실행돼요 ✅

# 작거나 같다, 크거나 같다는 <=, >=을 사용해요.

a = 3

if a > 2:
    print('a가 2보다 큽니다') # 언제나 실행돼요 ✅

if a == 2:
    print('a가 2와 같습니다.') # 언제나 실행돼요 ✅

# python에서 '같다'는 '==' 연산자를 사용해요.
```

### 논리연산자

```python
# 조건문에 여러 조건을 이어줄 수 있어요.

if 3 > 2 and 2 > 1:
    print('정답입니다.') # 언제나 실행돼요 ✅

if 3 > 2 or 2 < 1:
    print('정답입니다.') # 언제나 실행돼요 ✅

# 'and'는 '그리고', 'or'은 '또는'이라는 의미입니다.

# 혹은, 조건을 반대로 뒤집을 수도 있어요.

if not 3 > 2:
    print('정답입니다.') # 절대 실행지 않아요. ⛔️
```

### else, elif

```python
# 조건문을 조금 더 복잡하게 만들 수 있습니다.

a = 2

if a > 2:
    print('정답입니다.') # 절대 실행지 않아요. ⛔️
else:
    print('오답입니다.') # 언제나 실행돼요. ✅

# else 블럭 안에 있는 코드는 if 조건문을 통과하지 못했을 때만 실행됩니다.

if a > 3:
    print('a는 3보다 큽니다.') # 절대 실행지 않아요. ⛔️
elif a > 2:
    print('a는 2보다 큽니다.') # 절대 실행지 않아요. ⛔️
elif a > 1:
    print('a는 1보다 큽니다.') # 언제나 실행돼요. ✅
else:
    print('a는 1이거나 1보다 작습니다.') # 절대 실행지 않아요. ⛔️

# 각 조건들을 순서대로 거치면서 밑으로 내려갑니다.
# if, elif, else 중 가장 먼저 걸린 조건 하나만 실행됩니다.
```

### 함수

```python
# 함수는 코드 묶음입니다.

print('안녕하세요.')
print('반갑습니다.')

def hello():
    print('안녕하세요.')
    print('반갑습니다.')

hello()

# 안녕하세요.
# 반갑습니다.
```

### 매개변수

```python
# 위에서 만든 hello() 함수를 봅시다.
# 함수를 실행할 때 인사말을 바꿀 수 있다면 편하지 않을까요? 😆

def hello(greeting):
    print('안녕하세요.')
    print(greeting)

hello('환영해요.')

# 안녕하세요.
# 환영해요.

def sum(num1, num2):
    print(num1 + num2)

sum(1, 2) # 3

# 이렇게 함수 안에서 사용할 값을 함수를 실행할 때 넘겨줄 수 있습니다.
```

### 리턴문

```python
# 함수는 특정 동작을 실행할 뿐만 아니라 특정 값을 내보낼 수도 있습니다.

def sum(num1, num2):
    result = num1 + num2

    return result # num1과 num2를 더한 결과를 내보냅니다.

a = sum(1, 2) # a에 sum() 함수가 내보낸 3이 담깁니다.

print(a) # 3
```

## 고급 주제들

- f string 으로 깔끔한 print() 함수 사용하기.
- 언제나 if else 쌍을 사용해야 할까?🤔 깔끔한 조건문 만들기.
- 선언형 프로그래밍 vs 절차형 프로그래밍. 모듈화의 중요성.
