## 유체역학 시스템을 바라보는 관점

### 왜 시스템을 바라봐야 하는데?

우리가 유체역학을 배워야하는 이유는 무엇일까?

필자의 소견으로는 유체의 거동을 알고 그 특성을 활용하기 위함이라고 생각한다.

기계과의 관점에서 본다면 유체기계 설계나, 윤활과 같은 기술은 유체의 특성을 활용했음은 의심의 여지가 없다.

<br>

그렇다면 유체의 거동을 어떻게 알 것인가? 이는 유체를 분석해야 하고 이러한 분석 기법에는 또 다시 두가지로 나뉘게된다.

오늘 우리가 알아볼 것은 이런 유체의 거동을 보는 방법론 두가지 이다.

<br>

### Lagrangian description

첫번째는 아주 익숙한 방식, 이른바 입자 추적이다. 

전문적인 용어로는  **Lagrangian description**라고 한다.

그림으로 먼저 보도록 하자.

![https://res.cloudinary.com/dbzvbzksw/image/upload/v1589622928/0516posting/%EC%9D%B4%EB%AF%B8%EC%A7%80_2_ejrlut.png](https://res.cloudinary.com/dbzvbzksw/image/upload/v1589622928/0516posting/이미지_2_ejrlut.png)

<u>*<그림1>라그랑지안 그림자료 [1] [링크](https://youtu.be/iDIzLkic1pY)*</u> 

다음과 같이 한 입자를 시간 t에 따라 찍은 걸 합쳐 놓은 것이다. 즉 한놈만 패는 것이다.

우리는 보통 고체는 이런식으로 해석한다. 그 유명한 뉴턴 2법칙이 존재하기 때문이다.

F=ma로 해석하려면 m이 이러한 하나의 입자여야한다.

하지만 이러한 방식은 유체에서 밑천이 드러난다.

첫 번째로, 입자는 매우 작아서 그 움직임을 하나 하나하나 추적해서 정의하는건 굉장히 힘들다.

두 번째로, 입자는 continuum으로 가정하는데 continnuum이 뭔지 가볍게 알고 넘어가자

#### continuum

fluid는 입자로 구성되어있고 얘네들은 모여서 유체가 된다. 그러면 유체는 입자와 입자사이에 구멍이 날거니까 얘네들을 덩어리로 보는데는 엄밀히는 오류가 존재한다. 하지만 이는 상대적인 크기에 기반한다. 

우주 입장에서 보면 지구를 수소원자나 산소원자 단위로 보는 건 의미없다.

그냥 지구 한개로 퉁쳐버려도 상당히 후하게 쳐준것이다. 이러한 관점은 지구를 continuum이라고 보는 것이다. 

</br>

원래 얘기로 넘어와서 입자가 continuum인건 사실 자명하다. 우주까지 갈 필요도 없었다.

이런 입자끼리의 상호작용은 표현하기가 굉장히 힘들다. 물을 예로들은 반데르발스 결합을 했다가 풀어졌다가 하기 때문에 이런 걸 고려하기가 굉장히 까다롭기 때문이다.

###  Eulerian description

그래서 똑똑한 조상님들이 해결책을 만들어 놓았고 우리는 이에 숟가락만 얹으면 된다.

바로 오일러형님의 **Eulerian description** 이다.

![https://res.cloudinary.com/dbzvbzksw/image/upload/v1589622928/0516posting/%EC%9D%B4%EB%AF%B8%EC%A7%80_4_hfl3lz.jpg](https://res.cloudinary.com/dbzvbzksw/image/upload/v1589622928/0516posting/이미지_4_hfl3lz.jpg)

<u>*<그림2>오일러리안 그림자료 [1] [링크](https://youtu.be/iDIzLkic1pY)*</u> 

이는 어떤 control volume을 설정해두고 이 영역에 대한 사진을 찍는것이다.

이러한 방식은 내부에서 field variables란 걸 정해야하는데 이 변수는 시간과 위치에 따른 함수이다.

예를 들면 Pressure field, Velocity field 가 있다.

<br>
$$
P=P(x,y,z,t)
$$
<br>
$$
\vec V=\vec V(x,y,z,t)
$$
이때 스칼라와 벡터는 구분되어야한다.

이를 Cartesian 좌표계로 확장시켜보면 다음과 같다.

<br>
$$
\vec V=(u,v,w) = u(x,y,z,t)\vec i+ v(x,y,z,t)\vec j+w(x,y,z,t)\vec k
$$
<br>

이런 둘의 차이점은 책에서 이러한 예시를 통해 구별한다.

물이 흐르는 강에 서 있는 사람이 강의 흐름을 조사할 때 탐침을 한곳에 박아두고 측정하는 것을 오일러리안 디스크립션 

탐침을 흐르는 물에 띄워두고 움직이는 것을 라그랑지안 디스크립션이다.

오일러리안 디스크립션은 유체해석에 적합하나, 이는 명확한 거동에 대한 방정식이 있지 않으므로 구해져야한다.(라그랑지안은 뉴턴 2법칙이 있다.)

이는 레이놀즈 수송정리를 통해 얻어질 수 있고 이는 나중에 다시 알아보도록 하자.



### 느낀점

이러한 걸 처음 보는 순간 왜 이렇게? 라는 생각이 들었지만 다시금 리뷰를 해보고 이게 없었다면 이라는 가정을 두고 상상해보니 응당 그러하다라는 필요가 있는 관점이었다.

어떻게 입자를 바라볼 것인가? 는 사실 아주 지극히 정상적인 방식이다.

사진을 어떻게 찍을 것인가 어떤 구도로 찍을 것인가 어떤 삼각대로 찍을것인가? 이상한 질문처럼 보이는가?

우리는 항상 포장지에 속아 쉬움을 어려움으로 느끼고 있는지도 모른다.



[1] Understanding Lagrangian vs Eulerian approach - Fluid Mechanics  , https://youtu.be/iDIzLkic1pY