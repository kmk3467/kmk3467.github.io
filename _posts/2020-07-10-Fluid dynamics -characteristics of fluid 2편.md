# 유체의 특성 2편

## 7. 이상기체의 법칙

이상기체의 법칙은 열역학적인 변수가 서로 명확한 식으로 연결이 된다.



$$
P=\rho RT
$$



라는 식으로 정리가 되는데



### 7-1 절대압력

여기서 P는 절대압력이다. 이는 단위면적 당 수직으로 작용하는 힘을 이야기 한다.

기체의 경우는 내 손에 부딪힐 때를 가정한다면 내 손에 부딪힌 후 탄성충돌로 튕겨나가 부딪힐 때마다 힘으로 작용하기에

이를 일종의 압력으로 느끼게 된다. 

단위는 파스킬 Pa이며 1x1m^2 의 면적 당 1N의 힘이 작용하는 경우,

즉 1N = 1/9.81 kgf 이므로 약 100g의 무게가 누르는 아주 작은 정도의 힘이라고 할 수 있다.



###  7-2 기체상수

기체상수는 모든 기체에서 비열이 존재하는데 비열은 정압비열과 정적비열로 나뉜다.

이 둘의 크기 관계식은



$$
C_p \ge C_v
$$



이렇게 될 수 밖에 없는 이유는 체적을 제한시켰을 때 이동일이 들지 않기 때문에 1도를 올리는데 필요한 열량이 적게 든다.

R은

 

$$
C_p-Cv=R
$$



로 정의된다.

추가적으로 비열비 K는

 

$$
K=\frac {C_p}{C_v}
$$



가 되는데 공기의 비열비는 1.4정도가 된다. 

또한 이는 항상 1보다 크다.

결과적으로 기체상수 R은 



$$
[J/kg\cdot K]
$$



이 되는데 이러한 기체 상수는 1kg의 단위질량당 1도 올리는데 필요한 열은 얼마인가로 정의 할 수 있다.

여기서 왜 필요한 열이 되냐면 열역학 1법칙에 의해서 일과 열은 동등하기 때문이다.

각 기체마다 고유의 기체상수가 존재하는데

이를 비중량 [N/m^3]으로 나누면 Universal gas constant라는 일정한 수가 된다.



### 7-3 이상기체

이상기체는 기체의 분자를 완벽한 탄성구라고 가정한다.

테니스공같은 것이 완벽히 탄성충돌을 하며 아주 무작위적으로 움직인다.

그리고 이는 음속으로 움직인다.

이상기체의 상태는 기체의 모형도 같고 단위 부피당 개수도 같습니다. 

그래서 22.4L의 체적 속에 모든 이상기체의 분자 수는 6.023 *10^23개

즉 아보가드로 수만큼 존재하는데 차이는 무게이다.

수소는 분자량이 1이지만 헬륨은 2이므로 그 무게는 2배 무겁다.

우라늄 기체는 수소보다 235배 무겁고 산소는 16배 무겁다.

공기는 대부분 질소로 이루어져 있기에 쉽게 들 수 있지만 같은 체적 속에 우라늄 기체가 들어있다면 훨씬 무겁게 될 것이다.

이처럼 우리가 기체를 다룰 때 이상기체의 법칙이라는 아주 명확한 물리적 법칙이 존재하기에 비교적 쉽게 거동을 해석할 수 있다.



### 7-4 점성

![https://res.cloudinary.com/dbzvbzksw/image/upload/v1594358025/200710posting/KakaoTalk_20200710_141100357_fuzzd6.jpg](https://res.cloudinary.com/dbzvbzksw/image/upload/v1594358025/200710posting/KakaoTalk_20200710_141100357_fuzzd6.jpg)



우선 고체는 위의 그림처럼 전단력이 전단변형량에 비례하고

유체는 전단력이 전단변형률에 비례한다.

그리고 점성의 물리적인 의미는 전단력에 대한 저항정도를 의미한다.

(전단응력이므로 전단응력이 클수록 저항정도가 커진다.)





## 8. 유체의 압축성



### 8.0 압축성의 필요성

병에 담겨있는 유체를 상상할때 액체와 기체를 구분하기란 쉽지 않다.

이를 구분하기 위해 수치적으로 정량화할 필요성이 존재한다.

액체는 무겁고 기체는 가볍다고 하기에는 기체를 많이 압축시켜놓으면 마찬가지로 무겁다.

그러므로 이는 정량화 할 수 있는 수단이 아니다.

정량화 하는 대표적인 예는 체적계수 vulk modulus가 존재한다.



### 8.1 BULK MODULUS


$$
E_v=-\frac{dP}{\frac{d\forall}{\forall}} \qquad(1)
$$


![https://res.cloudinary.com/dbzvbzksw/image/upload/v1594360804/200710posting/%EC%9D%B4%EB%AF%B8%EC%A7%80_1_dkaxez.jpg](https://res.cloudinary.com/dbzvbzksw/image/upload/v1594360804/200710posting/이미지_1_dkaxez.jpg)



체적계수는 (1)과 같이 정의된다.

이에 대한 의미는 체적변화에 필요한 압력변화량이 된다.

**체적을 줄인다는 것을 압축을 의미하는데 압축이 되면 부피가 감소하게 된다. 그러므로 분모의 부호는 마이너스가 된다.**

체적탄성계수는 플러스가 되어야 하기 때문에 앞에 마이너스가 붙게된다. 



한편 질량의 미소변화는


$$
m=\rho V \\dm=d\rho V+\rho dV
$$


**하지만 압축을 하더라도 질량은 불변을 해야 해야하므로**


$$
dm=0=d\rho V+\rho dV  \\
d\rho V=-\rho dV \\
\frac {d\rho}{\rho}=-\frac{dV}{V} \qquad (2)
$$


그러므로 (2)식을 (1)식에 대입하면


$$
E_v=\frac{dP}{\frac{d\rho}{\rho}} \quad [N/m^2] \qquad (3)
$$


**이를 기체에 대해 대입하여 생각하면**

밀도 변화를 주기 위해 조그만 압력을 줘도 잘 변하므로 분자는 작고 분모는 크다.

**그러므로 체적계수는 작다.**

액체에 대해 대입하여 생각하면 상대적으로 큰 압력이 필요하고 분모는 작다

그러므로 체적계수는 크다

고체는 더욱 크다.

물질에 따라 체적탄성계수는 차이가 나므로 압축성유체와 비압축성 유체를 구분하는데 중요한 척도가 된다. 

실제로 예를 들면 대기압 상태에서 물의 체적을 1%정도 압축하는데 21.5Mpa의 압력이 필요로 한다. 

21.5Mpa은 21500KPa 이므로 약 대기압의 200배의 힘이 필요하다.

이는 1x1 m^2의 면적에 2,150,000 kgf의 무게가 누르고 있는 것과 같다.

### 8.2 등온과정에서  VULK MODULUS

**등온 과정에서** VULK MODULUS는 다음과 같다.


$$
P=\rho RT \\
T=const \\
then \\
\rho=\frac{P}{RT} \\
d\rho=\frac{dP}{RT} \quad (4) \\
\text{(4)식을 (3)식에 대입하면} \\
E_v=\rho RT = P
$$


즉 압력이 체적팽창계수가 된다.



### 8.3 등엔트로피 과정에서 VULK MODULUS

등엔트로피 과정은 열이 전달되지 않는 상태에서 압축이 된다.

실질적으로 등온과정보다 자주 있다.


$$
\frac{P}{\rho^k} =constant \qquad (5)
$$


이때 k는 비열비이다.

비체적은 밀도의 역수이므로


$$
\text{(5)식을 정리하면 } \\
P=\rho^k *const  \\
\frac{dP}{d\rho}=k\rho^{k-1}*const \\
(3)식에서 \\
E_v=\frac{dP}{d\rho}*\rho=k\rho^{k-1}*\rho*const\\
=k\rho^k*const=kP 
$$


표준공기 등 엔트로피 압축의 경우 k=1.4이므로

E_v=101.325kpa * 1.4 = 142kpa

물의 압축계수는 E_v=2150MPa이므로 물의 경우 압축이 굉장히 어렵다.

약 15140배 더 압력이 필요하다



## 9. 증기압(Vapor pressure)

### 9.1 포화증기압

포화증기압은 주어진 온도에서 액체가 기체로 변하는 압력이다.

반대로는 어떤 압력이 주어졌을 때 액체가 기체로 변하는 온도가 존재한다.

이러한 증기압은 증발이라는 현상을 일으킨다.



### 9.2 증발(Evaporation)

이러한 포화증기압은 증발을 발생시키는데

달톤의 분압법칙에 의해 대기압에서 수증기가 차지하는 압력은 매우 낮다.

그러므로 **표면에 있는 물**에서 액체상태는 대기압에서 낮은 압력으로 인한 낮은 끓는점으로

낮은 온도에서도 액체상태의 물이 수증기로 탈출할 수 있다.



### 9.3 비등 (Boiling)

boiling은 증발과 다르게 표면이 아닌 액체 내부에서 증기의 기포가 형성 되고 압력이 포화증기압에 도달 됐을 때 비등이 발생한다.

대기압에서는 물이 100도에서 비등을 하지만 해발 9000m에서는 기압이 30kPa이므로 69도에서 비등을 한다.

이것이 왜 중요하냐면 베르누이 방정식에 의해 물속에서 프로펠러가 운용될 때 속도가 높다면 압력이 낮아져야 한다.

이때 압력이 포화증기압보다 낮아지면 액체가 끓어 수증기가 된다. 

배를 타고 갈때 프로펠러 뒤에서 거품이 나오는 것은 그러한 원리인데 그러한 현상을 cavitation이라 한다.

즉, 고속 액체 유동에서 국소압력이 포화증기압보다 낮을 때 비등이 일어나느 현상을 공동현상이라 한다.



### 레퍼런스

[1] http://www.kmooc.kr/courses/course-v1:PNUk+FM_C01+2019_KM_010/course/ - KMOOK 김경천 교수님 19년 유체역학 강의노트

