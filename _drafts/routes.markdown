---
layout: post
title: Routes
tags: [ionic]
image: ''
---

## 페이지 이동 (Routes)

프로젝트를 생성하면 app/app-routing.modules.ts 파일에 아래와 같이 정의되어 있다.

```javascript
const routes: Routes = [
 { path: '', redirectTo: 'home', pathMatch: 'full' },
 { path: 'home', 
   loadChildren: './home/home.module#HomePageModule' },
];
```

routes 배열 안에 path를 지정해서, 페이지간 이동을 구현할 수 있는데, path 가 / 아래에 아무것도 없으면 /home 페이지로 리다이렉션한다.  
loadChildren Key에는 해당 path가 주어졌을 때, 수행될 module이 정의되어 있다.
조회된 결과 리스트를 선택함에 따라, 페이지 이동을 구현하기 위해서, path를 추가했다.

```javascript   
 { path: 'mysentences',
   loadChildren : './mysentences/mysentences.module#MysentencesPageModule' },
 { path: 'mysentences/:kr_id',
   loadChildren: './mysentences/mysentence-solutions/mysentence-solutions.module#MysentenceSolutionsPageModule'},
```

index.html의 body 부분을 보면 <app-root> 태그가 있는데, 이부분이 실제 html 코드로 변환 되어서 들어가고, index 페이지를 만들게 된다.
```html
<body>
 <app-root></app-root>
</body>
```

```html
<ion-app>
 <ion-router-outlet></ion-router-outlet>
</ion-app>
```


(참고) [https://ionicframework.com/blog/navigating-the-change-with-ionic-4-and-angular-router/]