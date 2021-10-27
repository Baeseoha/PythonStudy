# 코드업 파이썬 기초 100제 중 참고할만한 문제들 정리

print("Hello\\nWorld")

s = input()
print(s[0])
print(s[1])

s = input()
print(s[3:5])

# 분만 출력하기
s = input().split(':')
print(s[1])

#float 합 계산하기
a = input()
b = input()
a = float(a)
b = float(b)
print(a+b)


## 진수 출력

### 진수 출력

a = input()
n = int(a)            #입력된 a를 10진수 값으로 변환해 변수 n에 저장
print('%x'% n)  #n에 저장되어있는 값을 16진수(hexadecimal) 소문자 형태 문자열로 출력

<!-- #참고
#10진수 형태로 입력받고
#%x로 출력하면 16진수(hexadecimal) 소문자로 출력된다.
#(%o로 출력하면 8진수(octal) 문자열로 출력된다.)
#%X로 출력하면 16진수(hexadecimal)대문자로 출력된다.
#print('%o' % n)  #n에 저장되어있는 값을 8진수(octal) 형태 문자열로 출력

#16진수를 입력받아 8진수(octal)로 출력해보자.

#예시
#a = input()
#n = int(a, 16)      #입력된 a를 16진수로 인식해 변수 n에 저장
#print('%o' % n)  #n에 저장되어있는 값을 8진수(octal) 형태 문자열로 출력

#참고
#8진법은 한 자리에 8개(0 1 2 3 4 5 6 7)의 문자를 사용한다.
#8진수 10은 10진수의 8, 11은 9, 12는 10 ... 와 같다.
 -->
n = ord(input())
print(n)

참고
n = ord(input())  #입력받은 문자를 10진수 유니코드 값으로 변환한 후, n에 저장한다.

c = int(input())
print(chr(c))  #c에 저장되어 있는 정수 값을 유니코드 문자(chracter)로 바꿔 출력한다. 




* 부호 바꿔서 출력
n = int(input())
print(-n)

* a를 입력하면 b 출력

n=ord(input())

print(chr(n+1))

* 나누기 값
a, b = map(int, input().split())
print(a//b)

* 소수점 2째 자리까지 표현
a=float(input())
print( format(a, ".2f") )

f1, f2 = input().split()
f1 = float(f1)
f2 = float(f2)
print(f'{f1/f2:.3f}')

a, b = map(int, input().split())
print(a + b)
print(a - b)
print(a * b)
print(a//b)
print(a%b)
print(f'{a/b:.2f}')

예시
n = 10
print(n<<1)  #10을 2배 한 값인 20 이 출력된다.
print(n>>1)  #10을 반으로 나눈 값인 5 가 출력된다.
print(n<<2)  #10을 4배 한 값인 40 이 출력된다.
print(n>>2)  #10을 반으로 나눈 후 다시 반으로 나눈 값인 2 가 출력된다.

a, b = map(float, input().split())
print(a + b)

* not 사용

a = bool(int(input()))
print(not a)


* a, b 가 같지 않을 경우 True
a, b = map(int, input().split())
print(a != b)


* 둘다 참일경우
a, b = input().split()
print(bool(int(a)) and bool(int(b)))


a, b = map(int, input().split())
c = bool(int(a))
d = bool(int(b))
print((c and d) or ((not c) and (not d)))

a, b = map(int, input().split())
c = bool(int(a))
d = bool(int(b))
print((not c) and (not d)) or (not(c or d))

* ** 비트단위(bitwise) 연산자는,
* ~(bitwise not), &(bitwise and), |(bitwise or), ^(bitwise xor),
* <<(bitwise left shift), >>(bitwise right shift)
* 가 있다.

* 입력 된 정수를 비트단위로 참/거짓을 바꾼 후 정수로 출력해보자.
* 비트단위(bitwise)연산자 ~ 를 붙이면 된다.(~ : tilde, 틸드라고 읽는다.)

a = int(input())
print(~a)

* 정수값 두개 입력받아 큰 수 출력하기
a, b = input().split()
a = int(a)  #변수 a에 저장되어있는 값을 정수로 바꾸어 다시 변수 a에 저장
b = int(b)
c = (a if (a>=b) else b)
print(int(c))

ac = map(int, input().split())
for a in ac:
    if a % 2 == 0:
        print("even")
    else:
        print("odd")

n = input()
if n == 'A':
    print('best!!!')
elif n == 'B':
    print('good!!')
elif n == 'C':
    print('run!')
elif n == 'D':
    print('slowly~')
else:
    print('what?')

n = int(input())

if n//3==1 :
  print("spring")
elif n//3==2 :
  print("summer")
elif n//3==3 :
  print("fall")
else:
  print("winter")

* while

n = 1      #처음 조건 검사를 통과하기 위해 0 아닌 값을 임의로 저장
while n!=0 :
  n = int(input())
  if n!=0 :
    print(n)

n = int(input())
while n!=0 :
  print(n)
  n = n-1

* 입력받은 알파벳까지 차례로 출력
c = ord(input())
t = ord('a')
while t<=c :
  print(chr(t), end=' ')
  t += 1

* 78 번
* 영문 소문자 'q'가 입력될 때까지
* 입력한 문자를 계속 출력하는 프로그램을 작성해보자.

while True:
    x = input()
    print(x)
    if x == 'q':
        break











