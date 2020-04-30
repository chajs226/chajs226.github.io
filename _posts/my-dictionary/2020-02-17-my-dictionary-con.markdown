---
layout: post
title: My Dictionary-con..[Toy Project]
tags: [toy project]
categories: [Toy project]
comments: true
---
## Intro
아주 작은 것부터 시작하기로 했다. Cambly로 영어공부를 하면, tutor가  어색하거나 틀린 문장을 바로 잡아서 코멘트로 남겨주는데 영어 표현을 바로잡는데 꽤 쏠쏠한 재미가 있다. 문제는 이를 반복 연습해야 되는데, 몇일하다가 흐지부지 되거나, 오래전 연습했던 문장은 다시 까먹어버린다는 것이다.

해서, 누군가가 알아서 '이 문장 기억하니?'라고 물어봐주면 좋은데, 그런 거 물어봐주고 있을 사람이 있을리가 없다. 아주 수동적인 성향이라 나는 가만히 있고, 까먹을 때 쯤 알아서 물어봐주는 친구가 필요했다. 물론 메모를 해놓고 한번씩 메모를 열어서 공부할 수도 있겠지만, 몇일 지나면 메모를 열어봐야 된다는 것 자체를 100% 까먹는다.

또한, 한국에서 영어 공부가 어려운 이유는 일상 생활에서 의식해서 영어를 쓰기가 매우 어렵다는 것이다. 그래서 영어 공부 방법으로 영어로 일기쓰기, 영어 소설 읽기 등을 추천하지만, 극도의 의지가 필요하다.

그래서 이 App이 필요했다. 내가 연습했던 문장을 적어 놓으면, 시간이 되면 주기적으로 Notification으로 물어봐주는 App이다. 아주 기본적인 기능 구현부터 시작해서, 차츰 살을 덧붙여 언젠가는 Store에 공개할 수 있을 만큼 될 수 있기를 바란다.

## Release History
[2020.03.08]
- Fireabase를 통해서 notification을 받는 것을 구현했다. 이는 훌륭하신 분이 잘 설명해주신 tutorial을 참고했다. [Android Google FCM(Fire Base) 클라우드 메시징 푸시 사용하기](https://web-inf.tistory.com/21)
- 문제는 android app이 실행중이지 않거나, background로 실행중일 때는 notification을 받은 메시지를 acivity로 전달하지 못한다는 것이었는데, 역시 누군가가 아주 쉽게 설명해놓은 자료가 있었다. [Firebase Notifications in Background & Foreground in Android](https://wajahatkarim.com/2018/05/firebase-notifications-in-background--foreground-in-android/)
- foreground, background 상태에서는 메시지를 잘 받아서 전달한다. 그런데 app 이 kill 상태일때는? [kill 상태에서는 못받는게 정상이라고 한다.](ht
tps://blog.voidmainvoid.net/157)

[2020.03.20]
- App을 항상 백그라운드로 실행된 상태로 사용하고 있다.
- 메시지가 길어서 data 영역의 key-value하나에 다 담을 수 없는 경우가 있어서, body1, body2로 구분해서 FCM에서 데이터를 전송하고, 클라이언트에서 붙여서 표시되도록 수정했다.


[2020.04.06]
- FCM에 메시지를 최대 10개까지 주기적으로 push가 오도록 등록을 할 수 있는데, 어찌된 일인지 매일 3~4개정도 noti를 받는 문장만 오고, 나머지는 오지 않았다. 이를 해결하려는 것보다, 혼자서 메시지 등록해놓고 굳이 구글의 힘까지 빌려가며 noti를 받을 필요가 있나라는 현타가 왔고, 그냥 안드로이드 app의 로컬 SQLite를 쓰고, 타이머를 돌려서 시간되면 noti를 띄워주기는 걸로 바꾸끼로 했다. 위의 App은 여기서 종료.
- SQLite를 이용해서 안드로이드 앱을 만드는 기본적인 [튜토리얼](https://www.youtube.com/watch?v=p8TaTgr4uKM&list=PLS1QulWo1RIaRdy16cOzBO5Jr6kEagA07&index=2)을 참고 했다.


[2020.04.15]
- 문장등록 기능 구현
- noti를 언제받을지와 문장의 유효기간 설정을 위해서 날짜와 시간 입력이 필요한데, 아주 쉽게 설명된 블로그가 있어서 참고했다. [참고](https://gakari.tistory.com/entry/%EC%95%88%EB%93%9C%EB%A1%9C%EC%9D%B4%EB%93%9C-%EB%82%A0%EC%A7%9C-%EB%8C%80%ED%99%94%EC%83%81%EC%9E%90-%EC%8B%9C%EA%B0%84-%EB%8C%80%ED%99%94%EC%83%81%EC%9E%90-%EB%A7%8C%EB%93%A4%EA%B8%B0)


[2020.04.18]
- 등록된 전체 리스트는 리사이클러뷰를 이용하여 구현 [참고1](https://protocoderspoint.com/recyclerview-with-cardview-android-example-androidx-tutorial/), [참고2](https://lktprogrammer.tistory.com/169)
- 리사이클러뷰 아이템에 이벤트 거는 방법 [참고](https://recipes4dev.tistory.com/168)


[2020.04.24]
- v.2020.04.24
- 타이머를 사용하니, 등록된 문장이 처음에는 Noti로 잘 오다가 시간이 지나면 오지 않았다. 구글링을 해보니, 안드로이드 [백그라운드 정책](https://woovictory.github.io/2019/05/12/Android-Background-Policy2/) 떄문에 실행이 제한된다고 한다. 그래서 Alarm Manager를 사용하는 방식으로 뜯어고쳤다.
- Alarm Manager를 사용하는 방법은 여러 블로그와 안드로이드 개발 문서를 참고했다. [참고1](https://developer.android.com/training/scheduling/alarms) [참고2](https://m.blog.naver.com/PostView.nhn?blogId=jogilsang&logNo=221513058119&proxyReferer=https:%2F%2Fwww.google.com%2F) [참고3](https://lcw126.tistory.com/287)


[2020.04.30]
- v.2020.04.30
- 기 등록된 문장 수정 기능, Success, Fail, Skip 카운트 업데이트 기능 추가

GITHUB: https://github.com/chajs226/DailySentences