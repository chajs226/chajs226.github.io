---
layout: post
title: My Dictionary-05[Toy Project]
tags: [toy project, django, python]
categories: [Toy project]
---

## 기간
2019.08.18 ~ 2019.09.15

## 진행 계획
<details markdown="1">
<summary> 1차 release </summary>
1. Client 개발환경 구성 [완료]
2. Server 개발환경 구성 [완료]
3. Client 화면, 메뉴 설계 [1차완료]
4. 데이터 구조 설계 [완료]
5. Client-Server 통신 구성 [완료]
6. 서비스 개발
  - My Sentence 페이지 개발
    - 문장 등록하기
    - 등록된 리스트 조회 [완료]
  - Quiz 페이지 개발
    - 퀴즈 등록, 풀기
</details>
<details markdown="2">
<summary> 2차 release </summary>
6. 서비스 개발
  - 로그인 기능 개발
  - push 기능 개발
  - History 페이지 개발
</details>
<details markdown="3">
<summary> 3차 release </summary>
6. 서비스 개발
  - Settings 페이지 개발
  - Home 페이지 개발
</details>
<details markdown="4">
<summary> 4차 release </summary>
7. 추가 기능
  - 통계 기능 개선
  - 데이터 분석 관련
</details>

## 개발 내용
#### Client
- http request 구현
  - 클라이언트에서 post로 user_id를 던져서 내가 등록한 문장 리스트 가져오기


#### Server
- My Sentence 서비스 개발
  - 등록된 리스트 조회 서비스
    - 내가 등록한 리스트 가져오기(테이블 조인) [참고](http://scottlobdell.me/2015/01/sql-database-best-practices-django-orm/)
    - post로 user_id를 파라미터로 받아서 리스트 조회하기 [2]

## 삽질
- Access to XMLHttpRequest at 'http://localhost:8000/myDict/1' from origin 'http://localhost:8100' has been blocked by CORS policy: Response to preflight request doesn't pass access control check: No 'Access-Control-Allow-Origin' header is present on the requested resource.
  - url 정보가 같은 로컬서버에서 통신을 하려고 하면 CORS에러를 내뱉는데, 이를 허용하게 하는 설정을 아래의 사이트에서 보고 djanog에 설정을 했지만, 여전히 동일한 오류가 발생함)https://www.techiediaries.com/django-cors/)
- Forbidden (CSRF cookie not set.): 오류 발생
  - https://django.readthedocs.io/en/1.4.X/ref/contrib/csrf.html (여기 공부를 좀 하자. 일단 CROS 설정을 제거함.)
- Unexpected Token < in JSON at Position 0 에러 발생
  - https://www.codeproject.com/Tips/1239019/Unexpected-Token-in-JSON-at-Position
  - <QuerySet [..]> 형태의 데이터를 일반 json형태로 변경해서 처리했다. 결과를 List()로 씌우니까, QuerySet이 사라짐
- Angular에서 http post로 서비스를 요청하고, 그에 대한 결과값을 콜백으로 받기 위해 subscribe를 사용하는 부분을 완전히 잘못 사용하고 있었다. [참고](https://stackblitz.com/angular/ooqemvjyqkb?file=src%2Fapp%2Fheroes%2Fheroes.service.ts)를 보면서 구조를 뜯어고침

## 회고
Server 서비스를 만들고, Client에서 http 통신을 통한 결과를 화면에 뿌려주기까지 너무 많은 시간이 소요되었다. 그래도 일단 서비스 호출을 위한 하나의 사이클은 완성되었으니, 나머지 서비스를 만드는데 속도를 붙일 수 있을 것 같다. 문제는 앞으로 한달간 개인 프로젝트를 진행하기가 쉽지 않은 상황 때문에, 또 흐지부지될까 걱정이다. 앞으로 한달간 많은 시간을 투자하지는 못하더라도, 감을 잃지 않도록 조금씩이라도 들여다 볼 수 있도록 해야겠다.

## 다음 스텝
- My Sentence 페이지 개발
  - 문장 등록하기