---
layout: post
title: My Dictionary-03[Toy Project]
tags: [toy project, django, python]
---

## 기간
2019.08.11 ~ 2019.08.17

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
  - 클라이언트에서 post로 user_id를 던져서 내가 등록한 문장 리스트 가져오기 [3]


#### Server
- My Sentence 서비스 개발
  - 등록된 리스트 조회 서비스
    - 내가 등록한 리스트 가져오기(테이블 조인) [1] [참고](http://scottlobdell.me/2015/01/sql-database-best-practices-django-orm/)
    - post로 user_id를 파라미터로 받아서 리스트 조회하기 [2]

## 삽질
- Django ORM 에서 테이블을 조인걸려고 하다 보니, 테이블 설계가 이상한 것 같아서, 테이블을 모두 drop 하고 새로 생성하려고 했다. model.py 에서 자동 생성된 테이블의 키가 id인데, 굳이 kr_id 로 키를 주려다보니, 조인을 거는데 문제가 있는 것 같아서 기본 키를 갖도록 수정하려고 했다. 전부 drop하고 다시 migrate를 돌리니까.. 'django.db.utils.ProgrammingError: (1146, "Table 'mydict.mydictapp_krsentence' doesn't exist")' 에러가 발생함
- VS Code에 파이썬 from 에 'unable to import 'xxx' ' 오류가 발생.
  - ==> VS Code에서 python extension이 잘못된 pylint 버전을 사용해서 그렇다고 한다. venv 환경에서 'pip install pylint'로 pylint를 설치해서 해결했다.
- 테이블 설계가 잘못되어서, 모든 Table을 Drop하고 새로 생성하려고 하는데, makemigrations까지는 잘되었지만, 실제 migrate를 수행하면, 아래와 같이 변경될 것이 없다고 계속 나옴  
```
Operations to perform:  
  Apply all migrations: myDictApp  
Running migrations:  
  No migrations to apply.e
```
  - ==> [StackOverFlow](https://stackoverflow.com/questions/35494035/django-migrate-doesnt-create-tables/35494384)를 보고 해결. migration 폴더를 지우고, makemigrations를 다시 수행한 다음, 생성된 0001_inital.py 파일을 0001_manual.py 파일로 수정한다음 migrate를 수행

- Access to XMLHttpRequest at 'http://localhost:8000/myDict/chajs226@gmail.com' from origin 'http://localhost:8100' has been blocked by CORS policy: Response to preflight request doesn't pass access control check: No 'Access-Control-Allow-Origin' header is present on the requested resource.

## 회고


## 다음 스텝
