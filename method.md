# 잘 헷갈리는 파이썬 메소드 모음

### 연산자 사용 문자열 포맷팅

* %d   십진수 정수
* %f   실수
* %s   문자열
* %%   %  문자 자체

` "Hello %s" % ("파이썬")` -> 'Hello 파이썬'

` "My name is %s, I'm %d yrs old" % ( "박수지", 10) ` -> "My name is 박수지, I'm 10 yrs old"

` "원주율은 %.2f 입니다" % (pi) ` -> '원주율은 3.14 입니다'

` "***%4.2f***" % 0.12345  # %4.2f ` 전체적으로 4자리, 소숫점이하 2자리

` "My name is {}, I'm {} years old".format("박수진", 10) `

` "My name is {name}, I'm {age} years old".format(name = "박수진", age = 10) `

` ("PI = {:10.3f}".format(pi)) ` -> PI =      3.142

` f'Language: {lang}, Author: {author}' `

` f'Language: {lang:.2f}, Author: {author}' `

### map 사용
 ` a, b, c = map(int, input('3개의 정수 입력: ').split()) ` 
 
 ----
## 여러개의 데이터를 담는 타입
1. list   :  순서있다.  중복허용,  mutable
2. tuple  :  순서있다,  중복허용,  immutable
3. set : 순서없다,  중복허용안함
4. dict : key, value 쌍으로 구성, 순서없다.


## 역으로 list
`sorted(myStr, reverse=True)`

`result = "-".join(animals)` - 로 묶기

## random

` data = ['dog', 'cat', 'bird']
random.shuffle(data)
data `

* 로또 번호 추출 (shuffle 사용)
` data = [i + 1 for i in range(45)]
random.shuffle(data)
data[:6] `

## 쪼개기
` "apple"  -> ['A', 'P', 'P', 'L', 'E']

list(map(str.upper, list("apple"))) `

### 절대값
 ` list(map(absolute, [1, -2, -9]))`
 
### 리스트 값으로 입력받은 값 넣기
` list(map(int, input().split())) `

### filter
 ` list(filter(lambda x: x > 0, data)) `

### reduce 사용한 최대값 찾기
 ` dataset = [1, 4, 3, 5, 2] `
 reduce + lambda 를 사용하여 최댓값을 찾아보세요

` reduce(
    lambda a, b: a if a > b else b,
    dataset
)` 

* 각 아이템별 개수 구하기 reduce 파트에 있음


## for 문 사용 
range 안엔 숫자만
`s = input()
for i in s:
    print(i)`
    
`s = input()
for i in range(len(s)):
    print(s[i])`






















