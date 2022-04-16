# 챕터 3: 자료구조

이번주는 파이썬의 자료구조에 대해 다룹니다.

[동영상 🎬](https://www.youtube.com/watch?v=_CY4DlRCTBc&list=PLa7Lj786Q-Gts3-LsBl5I56YQrQb4sHxI&index=6)

## 요약 노트

```python
# 리스트의 더하기 연산

A = [1, 2, 3]
B = [4, 5, 6]
C = A + B
print(C) # [1, 2, 3, 4, 5, 6]
​

# 자유로운 파이썬의 리스트
# 문자열, 숫자, 심지어 다른 리스트도 리스트의 요소가 될 수 있어요.

mixedList = ["apple", 1, ["a", "b"]]​

# 리스트 인덱싱

fruits = ["apple", "banana", "mango"]
print(fruits[0]) # "apple" ➡️ 0부터 시작한다는 걸 잊지 마세요!
print(fruits[1]) # "banana"
print(fruits[2]) # "mango"
​

# 인덱싱을 이용해 특정 위치에 있는 요소를 바꿀 수 있어요.

fruits[0] = "pineapple"
print(fruits) # ["pineapple", "banana", "mango"]
​

# 유용한 리스트 관련 내장함수

test = [3, 2, 4, 1]
print(len(test)) # 4 ➡️ 리스트의 길이를 반환해요.
print(sort(test)) # [1, 2, 3, 4] ➡️ 리스트를 정렬해요.
print(sum(test)) # 10 ➡️ 리스트 안의 모든 값을 더해요.
​
# for문으로 리스트의 각 요소 순회하기

notebooks = ["macbook", "gram", "thinkpad"]
​
for notebook in notebooks:
    print(notebook)
# "macbook"
# "gram"
# "thinkpad"

​

# 기타 유용한 도구들

sports = ["football", "tennis"]

print(sports.index("tennis")) # 1 ➡️ 특정 요소의 인덱스를 반환해요.
print("baseball" in sports) # false ➡️ 특정 요소가 리스트 안에 있는지 검사할 수 있어요.

# 튜플

# 리스트와 거의 비슷해요.

fruits = ("banana", "apple")
print(fruits.index("banana")) # 0
print(fruites[1]) # "apple"
​

# 그러나 튜플은 한 번 만들고 난 이후 값을 변경할 수 없어요.

fruits[1] = "mango" # ⛔️ Error!
딕셔너리


# 딕셔너리

# 딕셔너리는 언제나 key: value 쌍으로 묶여 있어요.

# 과일 이름과 과일의 개수를 함께 나타내기. ⬇️
​
fruits = {
"apple": 2,
"banana": 4,
"mango": 2
}
​

# 딕셔너리는 key를 가지고 value를 얻을 수 있어요.

print(fruits["apple"]) # 2
​
# 딕셔너리 역시 in 연산자를 지원해요.

print("mango" in fruits) # True
​
# 딕셔너리의 key 전체, 혹은 value 전체를 출력할 수 있어요.

print(fruits.keys()) # dict_keys(['apple', 'banana', 'mango'])
print(fruits.values()) # dict_values([2, 4, 2])
​

# for문 안에 딕셔너리를 넣으면 모든 key들을 순회해요.
​
for key in fruits:
print(key, fruits[key])

# apple 2
# banana 4
# mango 2
```
