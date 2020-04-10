---
layout: post
title: Building Software Teams
categories: Note
tags:
---

<div class="ttbReview"><table><tbody><tr><td><a href="https://www.aladin.co.kr/shop/wproduct.aspx?ItemId=98546964&amp;ttbkey=ttbchajs2261707002&amp;COPYPaper=1" target="_blank"><img src="https://image.aladin.co.kr/product/9854/69/coversum/k292535351_1.jpg" alt="" border="0"/></a></td><td align="left"  style="vertical-align:top;"><a href="https://www.aladin.co.kr/shop/wproduct.aspx?ItemId=98546964&amp;ttbkey=ttbchajs2261707002&amp;COPYPaper=1" target="_blank" class="aladdin_title">유지보수 가능한 코딩의 기술 자바편</a> - <img src="//image.aladin.co.kr/img/common/star_s6.gif" border="0" alt="6점" /><br/>주스트뷔서 외 지음, 이일웅 옮김/길벗</td></tr></tbody></table></div>


목차를 보면서 지속적 통합, 배포, 코드 버전 컨트롤 등 그닥 흥미없는 내용은 skip 하고, 품질 측정 매트릭 작성, 테스트 자동화와 관련된 부분만 발췌해서 읽었다.

책이나 인터넷에 자료를 검색하거나, 타 사이트에 벤치마킹을 가서도 테스트 자동화를 효과적으로 운영하고 있는 것을 찾을 수 없었다. 다양한 시나리오를 담을 케이스를 작성하고(중요한 시나리오만 할지라도 노력이 많이 필요), 테스트 데이터 또한 만들어야 하고, 프로그램의 수정에 따른 자동화 테스트 프로그램(시나리오) 또한 유지보수 노력이 계속들어가게 된다. 그만큼 노력에 비한 효과를 얻기가 힘들다는 반증일 수 있다.

이 책에서 또한 인수 테스트 차원에서의 시나리오를 흘려보는 자동화 테스트 보다는(그것을 위한 도구가 있다는 것만 언급함. SOAPUI, Selenium, FitNesse 등을 활용할 수 있음), 단위 테스트를 잘 작성을 해야함에 비중을 두고 이야기 한다.
테스트 코드를 쓰는 것은 테스트 자체를 통한 프로그램 신뢰성 확보 뿐만 아니라, 개발자가 테스트 코드를 작성하면서 코드를 좀 더 심플하고 읽기 쉽게 작성하게 된다는 효과도 있다고 한다. 다만, 단위 테스트에서의 성공이 결합 테스트에서 성공할 것이라고 보장할 수 없기에, 이는 서로 상호 보완적으로 테스트가 계획되고 수행되어야 한다.

[품질 측정을 위한 매트릭 작성]
GQM(Goal, Quenstions, Metric)
1. 품질 측정 목표를 정하고,
2. 목표를 meet하는지 질문을 던지고,
3. Metric에 기반하여 답을 하여 측정한다.
주의할 점은 Metric을 너무 많이 가져가면 개발팀에서 아예 무시할 수 있고, 너무 단편적인 Metric은 잘못된 결론을 도출하게 될 수 있다.(단순히 코드라인 수 등)
개발팀에서 우선 목표를 어디에 두느냐에 따라, 무엇을 측정할지가 자연스럽게 정해진다.

목표를 정할 떄 고려할점
1. Object of examination
2. Purpose
3. Focus
4. Viewpoint
5. Enviornment
![buildingsoftwareteams](/images/posts/buildingsoftwareteams1.png)

그리고 목표에 대한 질문을 해야 한다. 가령, "유닛 단위의 복잡도가 코드 베이스 어느 영역에 존재하는지, 유닛의 복잡도가 변할 수 있는 데이터인지? 이를 해결하기 하느라 개발 일정상에 문제가 발생하지는 않는지?" 등

도움이 되지 않거나, 조직의 방향과 맞지 않는다면 과감히 측정지표를 버릴 수 있다. 그리고 측정할 수 있는 것을 측정하는 것이 아니라, 측정이 필요한 것을 측정해야 한다.