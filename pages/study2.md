# 2주차: 반복문

[학습 동영상 🎬](https://youtu.be/orzUaKSndII)

> 동영상에 나오는 repl은 예전 버전으로, 현재 버전과 다르게 생긴 부분들은 무시하셔도 됩니다.

이번주부터 스터디 앞 시간에 지난주 코딩 퀴즈 풀이를 진행합니다!

## 요약 노트

### for 반복문

```python
for i in range(10):
    print('hello')

# 'hello'가 10번 출력됩니다.

for i in range(10):
    print(i)

# 0,1,2,3,4,5,6,7,8,9가 순서대로 출력됩니다.

# range()함수는 시작값과 끝값을 지정할 수 있어요.

for i in range(3, 5):
    print(i)

# 3,4가 출력됩니다.

for i in range(1, 3):
    print(i)

# 1,2가 출력됩니다.
# range() 함수는 끝값 - 1 만큼 실행됩니다.
```

```python
# for 반복문을 사용해 간단한 구구단 출력기를 만들어봅시다.

def gugu(num):
    for i in range(1, 10):
        print(f'{num}*{i}={num*i}')

gugu(3)
```

### while 반복문

```python
i = 0

while i < 3:
    print(i)
    i += 1 # i = i + 1 과 똑같아요.

# 0,1,2가 출력됩니다.

while True:
    print('never run this code.⛔️')

# while 옆에 True를 적어주면 무한 반복문이 됩니다.
# 무한 반복문은 항상 종료 조건과 함께 써야 합니다.

i = 0

while True:
    if i > 3:
        break
    print(i)
    i += 1

 # 0,1,2,3,4가 출력됩니다.
 # 반복문은 break를 만났을 때 종료됩니다.

 for i in range(1, 11):
     if i % 2 != 0:
         continue
     print(i)

 # 1부터 10까지의 수 중에 짝수만 출력하는 반복문입니다.
 # 반복문이 continue를 만나면 밑의 코드를 실행하지 않고 바로 다음 반복으로 넘어가게 됩니다.
```

## 발전 과제

- `index`와 함께 반복해야 할 때 쓰는 `enumerate()`.
- 써먹을 곳 많은 이중반복문.
- 리스트 안에서 반복문 사용하기.
