---
layout: post
title: My Dictionary-08[Toy Project]
tags: [toy project]
categories: [Toy project]
---

## 기간
2019.12.09 ~ End

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
    - 문장 등록하기 [완료]
    - 등록된 리스트 조회 [완료]</span>
    - 로그인 기능 개발 <span style="color:blue"> [다음]
</details>
<details markdown="2">
<summary> 2차 release </summary>
6. 서비스 개발
  - push 기능 개발
  - History 페이지 개발
  - Quiz 페이지 개발
    - 퀴즈 등록, 풀기
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

## 회고
프로젝트를 중지했다. 핑계를 대자면 인생에 있어서 가장 큰 변화가 생기면서 이를 진행할 여유가 없기도 했고, 더 근본적인 이유는 언제나 그랬듯이 끈기 부족이었다.
그 끈기는 개인적인 노력으로 밀어부쳐서 유지될 수도 있겠지만, 더 중요한 것은 지속적인 흥미를 유발할 수 있는 동기가 필요한데 1차 release가 한없이 늘어지면서 자연스럽게 흥미를 잃어버렸다.

흥미 유지를 위해서는 처음 릴리즈 버전을 며칠이면 뚝닥할 수 있을 정도로 쪼개는 것이 중요하다. 아주 보잘 것 없더라도, 배포 가능한 형태의 눈에 보이는 결과물을 만들어 놓고, 이를 조금씩 덧붙여가는 방식을 따라야 하는데, 1차 release 버전을 능력에 비해 좀 크게 잡아놓은 것 같다.

해서, 이 프로젝트는 과감하게 접어버렸고, 당장 써볼 수 있는 아주 작은 프로그램을 만드는 것부터 다시 시작했다.
여러 블로그에 포스팅된 튜토리얼을 따라서 가장 기본적인 push 서비스를 만들었고, 매일 공부할 문장을 Android app으로 받아보고 있다. 단순하게 필요한 문장을 firebase에 접속해서 등록하고, 거기서 설정된 주기로 내 폰으로 push를 쏘고 있는데, 기능은 아주 보잘 것 없지만 여기가 출발점이 되어야 할 것 같다. 그리고 필요한 기능을 덧붙여서 자주 배포하는 것이다.

언제나 그랬듯이 이번에도 마침표를 찍진 못했다. 결과물이 없더라도 그 과정에서 의미있는 경험을 쌓는 것이 중요하다고 생각하는데(물론 결과물을 내는 것이 가장 중요함), django로 서버도 구축해봤고, 이를 나중에 다시 활용하면 다음엔 좀 더 빠르게 서버 구축이 가능할 것 같다. 그리고 javascript도 살짝 맛 볼 수 있었다.

아무튼, 실패. 끝.

## 다음 스텝
