## 크롤링 2탄 : 비동기로 속도를 빠르게 해보자 - 비동기란?

### 상황에 따른 속도차이

앞서 AJAX 홈페이지 기반에서의 로그인 하는 방식을 알아보았다.
하지만 여기서 프로그램을 가동해가며 큰 문제점을 발견하였다.
필자는 분명 속도를 빠르게 하기 위해 편의성을 버리고 Requests 모듈을 사용하였다.
하지만 특정 상황에서는 셀레니움 >> Requests 의 속도가 되는 상황을 발견하였다.

이러한 예를 들어보자
철수는 인터파크 티켓팅을 하려고한다. 
철수는 이러한 상황에서 해당 블로그를 보고 Requests 모듈을 활용한 웹크롤러를 제작하였다.
대망의 티켓팅 시간, 티켓팅을 하려는데 이게 왠걸.. 실행명령을 내렸는데도 한참을 기다렸다가 실패메시지를 띄우는 것이다. 여기서 왜 이렇게 되었을까?

#### 셀레니움의 방식 

```
    driver.find_element_by_id('user-id').send_keys(ide[i])
    driver.find_element_by_id('pwd').send_keys(pw[i])
    driver.find_element_by_class_name("btn-login").click()
    driver.implicitly_wait(3)
```

셀레니움은 click()이라는 함수를 사용한다.
이 말인 즉슨 한번 클릭 후 니가 어찌되든 신경 안쓰고 내 일만 하겠다는 뜻이다.

### Requests의 방식

```
first_page.append(s[i].get("http://www.GAMEURL.co.kr/login",headers=headers))
       login_req=s[i].post('http://www.GAMEURL.co.kr/ajax/_member_process',data=LOGIN_INFO[i])
```

 이 친구는 좀 다르다.
나는 GAMEURL홈페이지에 _member_process페이지에 내 로그인 정보를 전송 한 후 서버의 응답을 받고 난후 움직이는 친구이다.
이는 간단하게 login_req.status_code 명령을 통해 작동방식을 추론해볼 수 있다.

이를 통해 어떤 특정시간대에 서버에 요청이 몰린다면 서버는 그에 대한 답장을 해주는데 시간이 오래 걸릴 것이다. 그렇다면 나(크롤러)는 거기서 멍청하게 기다리고 있어야 하기 때문에 다소 느리더라도 일방적으로 클릭이라는 정보만 보내는 셀레니움보다 느리다는 것이다.

## 작동방식이 다른건 알겠다. 그러면 어쩌라고?

결론부터 말하면 우리는 비동기화 기법을 사용해야 한다.
서버의 응답을 보내고 그 답장을 받을때까지 기다리는 건 셀레니움보다 크롤러를 느리게 만든다.
이를 해결할 방법은 여러군데 요청을 보내놓고 답장을 먼저 받은 순서대로 처리해주는 것이다.

이는 컵라면을 10개 끓이는 것으로 예를 들 수 있다.
동기화 방식은 컵라면1개를 끓인다 -> 완료된다. -> 컵라면 1개를 더 끓인다. -> 완료된다. -> 컵라면 1개를 더 끓인다.->완료된다의 형식을 따른다. 이는 직관적으로 충분히 비효율적으로 보인다.

비동기화 기법은 컵라면 1개를 끓인다-> ... 나머지 9개의 컵라면을 끓인다. 완료되는 순서대로 완료시킨다.
당연하게도 이게 일상생활에서의 우리의 행동양식이다. 이것만 보더라도 컴퓨터가 얼마나 멍청한지 알 수 있다.

다음 편 3편은 간단한 예제를 통해 동기화 기법과 비동기화 기법을 비교해보고 4편을 통해 실질적으로 1편에서의 로그인크롤러를 어떻게 개선시키고 테스트를 통해 얼마나 빨라졌는지 확인해보도록 하자.