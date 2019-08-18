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
5. Client-Server 통신 구성 [진행]
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
- N/A

#### Server
- 데이터 구조 재구성
  - 임의로 생성한 key 제거. Django ORM에서 제공하는 기본 키를 사용하는 것으로 변경
- My Sentence 서비스 개발
  - 등록된 리스트 조회 서비스
    - 내가 등록한 리스트 가져오기(테이블 조인) [참고](http://scottlobdell.me/2015/01/sql-database-best-practices-django-orm/)

## 삽질
- Django ORM 에서 테이블을 조인걸려고 하다 보니, 테이블 설계가 이상한 것 같아서, 테이블을 모두 drop 하고 새로 생성했다.(model.py 에서 자동 생성된 테이블의 키가 id인데, 굳이 kr_id 로 키를 주려다보니, 조인을 거는데 문제가 있는 것 같아서 기본 키를 갖도록 수정하려고 함) 테이블을 모두 drop하고 다시 migrate를 돌리니까 에러가 발생했다.
  ```
  'django.db.utils.ProgrammingError: (1146, "Table 'mydict.mydictapp_krsentence' doesn't exist")'
  ```
  - ==> 테이블명까지 모두 다시 바꾸고, makemigrations와 migrate를 수행하니까, 위의 에러는 발생안했지만, 아래와 같이 변경될 사항이 없다고 계속 나왔다.
  ```
  Operations to perform:
  Apply all migrations: myDictApp
  Running migrations:
  No migrations to apply.e
  ```
    - ==> [StackOverFlow](https://stackoverflow.com/questions/35494035/django-migrate-doesnt-create-tables/35494384)를 보고 해결. migration 폴더를 지우고, makemigrations를 다시 수행한 다음, 생성된 0001_inital.py 파일을 0001_manual.py 파일로 수정한다음 migrate를 수행하니 해결되었다.

- VS Code에 파이썬 from 에 'unable to import 'xxx' ' 오류가 발생했다.
  - ==> VS Code에서 python extension이 잘못된 pylint 버전을 사용해서 그렇다고 한다. venv 환경에서 'pip install pylint'로 pylint를 설치해서 해결했다.

## 회고
테이블 설계가 명확하지 않으니, 서비스를 개발하면서서 테이블 설계를 변경하게 되고, 앞단의 작업을 계속 반복하게 되었다. 그 와중에 오류가 발생하고, 오류를 해결하느라, 한주를 다 보내게 되었다. 결국, 이번주에 목표로 했던 클라이언트-서버간 통신까지 마무리 하지 못했다. 서버단의 리스트 조회하는 샘플 서비스까지는 성공했으니, 다음주에는 실제 클라이언트에서 post 서비스를 호출하는 부분까지 완성해야겠다.

## 다음 스텝
- http request 구현
  - 클라이언트에서 post로 user_id를 던져서 내가 등록한 문장 리스트 가져오기

- My Sentence 서비스 개발
  - 등록된 리스트 조회 서비스
    - post로 user_id를 파라미터로 받아서 리스트 조회하기