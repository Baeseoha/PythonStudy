# 연습: Taxi 클래스 설계

## 문제
'택시'에는 승객들에게 공통적으로 적용되는 자료
- 택시 요율 (거리당 요금)  : 700 ( 거리 1km 당 요금 )
- 기본 요금 : 3000
- 최초 기본 주행 거리 : 2km 

택시 객체 생성시 승객별로 돈과, 거리를 받아서 생성

거리에 따른 요금 계산 메소드 정의
거리에 따른 잔돈 계산 메소드 정의

## 내가 푼 답
`class Taxi:
    fee = 700 # 택시 요율
    base = 3000 # 기본요금
    distance = 2 # 기본 주행 거리
    
    def __init__(self, money, goal):
        self.money = money
        self.goal = goal
        self.total_wage = 0
        # 거리에 따른 요금 계산
        if goal > self.distance:
            self.total_wage = Taxi.base + ((goal - 2) * Taxi.fee)
        else:
            self.total_wage = Taxi.base
        # 잔돈 계산
        self.change = money - self.total_wage
        print("비용은?", self.total_wage)
        print("잔돈은?", self.change)`

입력값 `Taxi(30000, 10)`
출력 값 
비용은? 8600
잔돈은? 21400






