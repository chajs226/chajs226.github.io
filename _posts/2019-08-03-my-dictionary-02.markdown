---
layout: post
title: My Dictionary-02[Toy Project]
tags: [toy project, django, python]
---

## 기간
2019.07.28 ~ 2019.08.03

## 개발 내용
#### Client
  - ~~한글 문장을 선택했을 때, 등록된 영어 문장 불러오기 (완료)~~
  - ~~문장 등록하기 버튼 추가 (완료)~~
    - ~~새문장 등록 페이지 구현 (완료)~~
      - 한글 문장 입력 전송 후, 입력된 한글 문장을 조회하고 영어 문장 입력 버튼을 눌러서, 답을 바로 입력하는 화면 구현 (향후 추가)
  - ~~퀴즈 풀기 페이지 구현 (완료)~~
  - http request 구현 (예정)

#### Server
  - Django 환경 셋팅
    - Python 가상 환경 및 Django 설치 참고 블로그: [링크]([https://hongku.tistory.com/258)
      - 앞으로 Django는 항상 가상환경 위에서 실행을 하게 된다.
        - 가상환경을 설치한 경로(C:\...\myDjango)에서 가상환경을 실행('myvenv\Scripts\activate')시키고, Django 프로젝트를 생성한 경로(...\myDictServer) 'python manage.py runserver'로 서버 실행
  - 프로젝트 생성 튜토리얼: [링크](https://docs.djangoproject.com/ko/2.2/intro/tutorial01/)
    - mySQL 설치 & 설정
      - 가상환경을 설치한 경로(c:\...\myDjango)에서 'pip install mysqlclient' 로 mysql driver 설치
      - setting.py 에 mysql 설정값(DB명, IP/PORT, 계정, 비번 등)을 기술
        ```python
        DATABASES = {
          'default': {
              'ENGINE': 'django.db.backends.mysql',
              'NAME': 'mydict',
              'HOST': '127.0.0.1',
              'PRT': '3306',
              'USER': '???',
              'PASSWORD': '???',
            }
        }
        ```
    - 모델을 만들고, 테이블 생성, 샘플 데이터 생성 (완료)
      - models.py - 모델 생성 및 변경
      - python manage.py makemigrations - 변경사항에 대한 마이그레이션 생성
      - python manage.py migrate - 변경사항을 데이터베이스에 적용
    - 관리자 페이지 생성 완료 (완료)
    - 한글 문장 가져오는 서비스 개발 (진행)

## 삽질
- mysqlclient 설치 오류
  - 오류 메시지: error: [WinError 3] 지정된 경로를 찾을 수 없습니다: 'C:\\Program Files (x86)\\Microsoft SDKs\\Windows\\v8.1\\lib'
    - 해결방법: 원인은 모르겠으나, 구글링해서 Mysqlclient whl파일을 로컬에 직접 내려받아서 설치했다.
      - mysqlclient 다운로드: [링크](https://www.lfd.uci.edu/~gohlke/pythonlibs/#mysqlclient)
      - 설치방법: pip install {다운받은 파일}

## 회고
Django 환경 설정을 하면서 한주가 지나갔다. Django 환경을 구성하면서 다른분들이 잘 정리해놓은 tutorial이나 공식 기술 페이지가 큰 도움이 되었다. 이번에 만들려는 앱이 단순한 CRUD로 대부분의 기능 구현이 가능하기 때문에 차주에 Client, Server 간의 통신하는 부분까지 진도가 나가면, 기본적인 틀은 빠르게 만들 수 있을 것이다. 그리고 이를 기반으로 좀 더 흥미로운 주제에 대해서 파고들 수 있을 것 같다.

## 다음 스텝
- Client와 Server간에 http를 통한 데이터 전송 부분 구현
  - 한글 문장 등록, 그에 대한 영어문장 등록 기능 구현
  - MySentences 리스트 조회하기 구현