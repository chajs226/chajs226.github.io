---
layout: post
title: My Dictionary-03[Toy Project]
tags: [toy project, django, python]
---

## 기간
2019.08.18 ~ 2019.08.31

## 진행 계획
<details markdown="1">
<summary> 1차 release </summary>
1. Client 개발환경 구성 [완료]
2. Server 개발환경 구성 [완료]
3. Client 화면, 메뉴 설계 [1차완료]
4. 데이터 구조 설계 [완료]
5. Client-Server 통신 구성
6. 서비스 개발
  - My Sentence 페이지 개발
    - 문장 등록하기
    - 등록된 리스트 조회
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
  - url 정보가 같은 로컬서버에서 통신을 하려고 하면 CORS에러를 내뱉는데, 이를 허용하게 하는 설정을 아래의 사이트에서 보고 djanog에 설정을 했지만, 여전히 동일한 오류가 발생하고 있음 )https://www.techiediaries.com/django-cors/)
- Forbidden (CSRF cookie not set.): 오류 발생
  - https://django.readthedocs.io/en/1.4.X/ref/contrib/csrf.html 여기공부를 좀 하자. 일단 CROS 설정을 제거함.


## 회고


## 다음 스텝
- Ionic Post Reqest 다시 확인해서 구현하기(Rclient에서는 서비스 요청을 제대로 받는것을 봐서는,, ionic에서 post 요청에 문제가 있는 것 같음). 아니면 localhost에서 호출하는 것때문에 문제가 발생할지도...
  - Unexpected Token < in JSON at Position 0 에러 발생
    - https://www.codeproject.com/Tips/1239019/Unexpected-Token-in-JSON-at-Position 다시 확인