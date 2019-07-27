---
layout: post
title: My Dictionary-01[Toy Project]
tags: [toy project]
---

## 기간
2019.07.21 ~ 2019.07.27

## 개발 내용
- Client
  - 한글 문장을 선택했을 때, 등록된 영어 문장 불러오기 (완료)
  - 문장 등록하기 버튼 추가 (완료)
    - 새문장 등록 페이지 구현 (완료)
      - 한글 문장 입력 전송 후, 입력된 한글 문장을 조회하고 영어 문장 입력 버튼을 눌럿, 답을 바로 입력하는 화면 구현 (향후 추가)
  - 퀴즈 풀기 페이지 구현 (완료)
  - http request 구현 (차주 예정)

- Server
  - Django 환경 셋팅 (차주 예정)

## 스터디 내용
- [Route 정리]({% post_url 2019-07-28-route %})

## 삽질
- Object 를 가지고 *ngFor 를 돌리는데, array로 생각하고 처리를 하려다 보니, 계속 오류가 발생. Object를 html 페이지에서 for문 처리 하는데 시간 소요
    - 오류메세지: Cannot find a differ supporting object '[object Object]'
    - 해결방법
      ```html
        <ion-list>
         <ion-item *ngFor="let en of loadedMyEnSentence | keyvalue">
           {{ en.value.en_st }}
         </ion-item>
        </ion-list>
       ```

## 회고
우선 클라이언트 단의 간단한 화면을 먼저 구성하였다. 샘플 데이터를 서비스 단에 array로 만들어 놓고, 그것을 화면에 보여주는 부분에 집중하였다. Angular, Javascript, Ionic 등 클라이언트 단에서 사용하는 기술들을 모두 처음 접하다보니, 개념을 이해하는게 쉽지 않았는데, 아직 익숙하지 않다. 그래도 경험상 각각을 공부해서 프로젝트를 진행하는 것보다, 부딪혀보고 필요한 부분을 찾아서 공부하는게 더 낫기 때문에 일단 맨땅에 헤딩을 시작했다.

그래도 문제를 해결해가는 과정에서 알게된 정보나 기술은 중간중간 정리가 필요할 것 같다. 아까운 삽질의 시간에서 조금이라도 얻는 것이 있어야 할 것이다.

차주에는 서버 환경을 구성해서, 간단한 데이터가 Client-Server 간에 주고 받는 것까지 구현하는 것이 목표다.

## 다음 스텝
- Client
  - http request 구현
- Server
  - Django 환경 셋팅