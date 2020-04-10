---
layout: post
title: My Dictionary-con..[Toy Project]
tags: [toy project]
categories: [Toy project]
comments: true
---
## Intro
아주 작은 것부터 시작하기로 했다. Cambly로 영어공부를 하면, tutor가  어색하거나 틀린 문장을 바로 잡아서 코멘트로 남겨주는데 영어 표현을 바로잡는데 꽤 쏠쏠한 재미가 있다. 문제는 이를 반복 연습해야 되는데, 몇일하다가 흐지부지 되거나, 오래전 연습했던 문장은 다시 까먹어버린다는 것이다.

해서, 누군가가 알아서 '이 문장 기억하니?'라고 물어봐주면 좋은데, 그런 거 물어봐주고 있을 사람이 있을리가 없다. 아주 수동적인 성향이라 나는 가만히 있고, 까먹을 때 쯤 알아서 물어봐주는 친구가 필요했다. 물론 메모를 해놓고 한번씩 메모를 열어서 공부할 수도 있겠지만, 언급했듯이 나는 아주 수동적이다.

또한, 한국에서 영어 공부가 어려운 이유는 일상 생활에서 의식해서 영어를 쓰기가 매우 어렵다는 것이다. 그래서 영어 공부 방법으로 영어로 일기쓰기, 영어 소설 읽기 등을 추천하지만, 극도의 의지가 필요하다.

그래서 이 App이 필요했다. 내가 연습했던 문장을 적어 놓으면, 시간이 되면 주기적으로 Notification으로 물어봐주는 App이다. 아주 기본적인 기능 구현부터 시작해서, 차츰 살을 덧붙여 언젠가는 Store에 공개할 수 있을 만큼 될 수 있기를 바란다.

## Release History
[2020.03.08]
- Fireabase를 통해서 notification을 받는 것을 구현했다. 이는 훌륭하신 분이 잘 설명해주신 tutorial을 참고했다. [Android Google FCM(Fire Base) 클라우드 메시징 푸시 사용하기](https://web-inf.tistory.com/21)
- 문제는 android app이 실행중이지 않거나, background로 실행중일 때는 notification을 받은 메시지를 acivity로 전달하지 못한다는 것이었는데, 역시 누군가가 아주 쉽게 설명해놓은 자료가 있었다. [Firebase Notifications in Background & Foreground in Android](https://wajahatkarim.com/2018/05/firebase-notifications-in-background--foreground-in-android/)
- foreground, background 상태에서는 메시지를 잘 받아서 전달한다. 그런데 app 이 kill 상태일때는? [kill 상태에서는 못받는게 정상이라고 한다.](https://blog.voidmainvoid.net/157)
[2020.03.20]
- App을 항상 백그라운드로 실행된 상태로 사용하고 있다.
- 메시지가 길어서 data 영역의 key-value하나에 다 담을 수 없는 경우가 있어서, body1, body2로 구분해서 FCM에서 데이터를 전송하고, 클라이언트에서 붙여서 표시되도록 수정했다.
[2020.04.06]
- 굳이 FCM을 사용할 이유가 없어서, 로컬의 SQLite를 사용해서 타이머로 push 팝업을 띄우는 방식으로 변경
- Table(https://www.youtube.com/watch?v=p8TaTgr4uKM&list=PLS1QulWo1RIaRdy16cOzBO5Jr6kEagA07&index=2)
    - id:int, kor_setnece:varchar[1000], eng_sentence:varchar[1000], start_date:date, end_date:date, sucess_count:int, fail_count:int, skip_count:int, popup_time:varchar[4]


- ToDo
  - app을 항상 실행 상태로 만들기 or 위젯형태로 만들어서 항상 띄워놓기
  - android 화면 디자인 해서 다듬기(화면 펼침)
  - 서버 구축?