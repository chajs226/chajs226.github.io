---
layout: post
title: My Dictionary-05[Toy Project]
tags: [toy project, django, python]
categories: [Toy project]
---

## 기간
2019.10.27 ~ 2019.11.03

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



#### Server

## 삽질

## 회고

## 다음 스텝
- My Sentence 페이지 개발
  - 영어문장 가져오기
    - 한글 리스트는 DB에서 가져오고 있는데,, 영어 문장 가져오는 건 아직 미개발상태
      - urls.py에 한글 문장을 클릭했을 때, 영어를 가져오는 서비스 path를 정의하고, 서버쪽 서비스 개발해야 함. 그리고 클라이언트에서 자체 리스트 데이터가져오는걸 제거하고, 서버로 http서비스 호출하고 리턴받는 부분 개발해야함.
  - 문장 등록하기


