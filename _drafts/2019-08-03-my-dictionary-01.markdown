---
layout: post
title: My Dictionary-02[Toy Project]
tags: [toy project]
---

## 기간
2019.07.28 ~ 2019.08.03

## 개발 내용
- Client
  - ~~한글 문장을 선택했을 때, 등록된 영어 문장 불러오기 (완료)~~
  - ~~문장 등록하기 버튼 추가 (완료)~~
    - ~~새문장 등록 페이지 구현 (완료)~~
      - 한글 문장 입력 전송 후, 입력된 한글 문장을 조회하고 영어 문장 입력 버튼을 눌럿, 답을 바로 입력하는 화면 구현 (향후 추가)
  - ~~퀴즈 풀기 페이지 구현 (완료)~~
  - http request 구현 ()

- Server
  - Django 환경 셋팅 ()
    - Python 가상 환경 및 Django 설치 참고 블로그: https://hongku.tistory.com/258
      - 앞으로 Django는 항상 가상환경 위에서 실행을 하게 된다.  
          예) C:\...\myDjango 경로(=가상환경을 설치한 경로)에서 'myvenv\Scripts\activate' 가상환경을 실행시키고, myDictServer 경로(=Django 프로젝트를 생성한 경로)에서 'python manage.py runserver'로 서버 실행
    - 프로젝트 생성 튜토리얼: https://docs.djangoproject.com/ko/2.2/intro/tutorial01/
    - mySQL 설치 & 설정
      - ~\myDjango 경로(=가상환경을 설치한 경로)에서 'pip install mysqlclient' 로 mysql driver 설치
      - setting.py 에 설치된 mysql 설정값(DB명, IP/PORT, 계정, 비번 등)을 기술하고, 'python manage.py migrate' 를 통해 app 관리를 위한 기본 테이블들을 생성 
        ```python
        DATABASES = {
          'default': {
              'ENGINE': 'django.db.backends.mysql',
              'NAME': 'mydict',
              'HOST': '127.0.0.1',
              'PRT': '3306',
              'USER': 'mydict',
              'PASSWORD': 'mydict',
            }
        }
        ```
    - 튜토리얼 모델만들기 할 차례

## 스터디 내용
- 

## 삽질
- mysqlclient 설치 오류
  - 오류 메시지: error: [WinError 3] 지정된 경로를 찾을 수 없습니다: 'C:\\Program Files (x86)\\Microsoft SDKs\\Windows\\v8.1\\lib'
  - 해결방법: 원인은 모르겠으나, 구글링해서 Mysqlclient whl파일을 로컬에 직접 내려받아서 설치했다. 
    - mysqlclient 다운: https://www.lfd.uci.edu/~gohlke/pythonlibs/#mysqlclient
    - 설치방법: pip install {다운받은 파일}

## 회고

## 다음 스텝
- Client
  - http request 구현
- Server
  - Django 환경 셋팅