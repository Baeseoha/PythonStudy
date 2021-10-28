## 타이타닉, 리스트에 결과값 넣기

`from functools import reduce
f = open("../../../dataset/titanic.csv", 'r')
lines = f.readlines()
f.close()
vive = []

for line in lines[1:]: # 첫 라인 제거
   
    line = line.split(",") # line 을 , (콤마) 로 쪼개기 (split())
    line = line[1:3] # 생존여부, 객실등급 데이터 추출 ([1],[2]번째 데이타)
    vive.append(line)

print(vive)

 class 별로 사람 수 
vive1 = 0
vive2 = 0
vive3 = 0

for i in vive:
    vclass = i[1]
    print(pclass)   
    if '1' == vclass:
        vive1 += 1
    elif '2' == vclass:
        vive2 += 1
    elif '3' == vclass:
        vive3 += 1
print(vive1, vive2, vive3)

s1 = 0
s2 = 0
s3 = 0


for survive in vive:
    #print(survive)
    if '1' == survive[1]:
        if '1' == survive[0]:
            s1 += 1
    elif '2' == survive[1]:
        if '1' == survive[0]:
            s2 += 1
    elif '3' == survive[1]:
        if '1' == survive[0]:
            s3 += 1
print(s1, s2, s3)

3등급] 총 491 명, 생존 119 명, 생존률 24.2%

print(f' 1등급] 총 {vive1}명, 생존 {s1} 명, 생존률{(s1/vive1) * 100:.2f}%')
print(f' 2등급] 총 {vive1}명, 생존 {s1} 명, 생존률{(s2/vive2) * 100:.2f}%')
print(f' 3등급] 총 {vive1}명, 생존 {s1} 명, 생존률{(s3/vive3) * 100:.2f}%')`
