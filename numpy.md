# numpy

## scalar
Scalar : 0차원 array (단일값)

Vector : 1차원 array

Matrix : 2차원 array

Tensor : 3차원(이상) array
- 1 차원 array(벡터) 생성
`x = np.array([1, 2, 3])`

## shape, size, ndim len(), dtype
.shape - 차원, 몇개의 데이터로 구성되어있는지
.size - 데이터의 개수
.ndim - 차원
np.arange(3, 10, dtype=np.int16) - 데이터 타입 명시 가능 

## rand(), randn() 차이
rand() 는 uniform 한 분포에서 값을 가져오고

randn() 은 normal distribution 에서 값을 가져온다

#### 로또 번호 생성기

`def generate_lotto_nums():
    d = np.arange(1, 46)
    np.random.shuffle(d)
    return d[:6]
generate_lotto_nums()`

## 축 바꾸기
a.T

## 최댓값, 최솟값
np.max(y2)
np.min(y2)



np.argmax(y2, axis=0) - y축으로 최댓값 불러옴 (세로 )

### 조건

np.where(q > 0, q, 0)









