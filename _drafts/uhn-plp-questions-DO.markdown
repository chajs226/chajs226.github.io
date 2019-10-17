---
layout: post
title: Quenstions
categories: UHN-PLP
---

### To-Do
[로리]
- HL7의 ADT형태로 데이터를 전달하더라도, 요청 시스템별로 조금씩 다른 형태의 데이터를 요청하지 않나? 굉장히 아이디얼한 개념인것 같은데.

- 너희팀의 다른 이들은 어떤일을 담당하나?

[토니질문]
- 캡처 새로받기 - (화면생성, 배포시 requestID 물고 승인한부분, PC타임아웃설정, 사용자설명서가이드-목차부분도)
  - I'm making presentation metrials of PLP.
    Can I get some screenshots?
    - the screen which is when you are making new screen, you configure new screen
    - the screen which is that you set up the pc timeout
    - the screen which is when you release the application, you approve the release rquest. I think I saw the approve history and user request id.
    - the screen which is for user guide on the web.

- 운영배포할때 1년에 8번 벤더에서 지원을 들어오나?
  - When you release EPR to live system, Does venders visit here and support to digital team?
    - ====> 메이저 업그래이드일때만 벤더가 들어옴. 핵심 기능 변경에만. 년 8회 배포에서 화면 수정, 추가로 인한 작업은 디지털팀에서 직접 처리함

- 온콜당직 돌아가면서 하는건가
  - You said that during the daytime, two people receive the call from the helpdesk or user, and during the night time, one person receives the call. So, Do they work by turn?
    - 돌아가면서하고.. 이슈가 등록되면 당직자 모바일로 바로 노티가 간다.

- 화면 갯수, EPR이 커버하고 있는 영역
  - Do you know how many screens are in EPR?
    -> 수천개이다. 모른다.

- OPR문서는 헬프데스크에서 보는건지? 온콜 당직자가 보는건지?
  - Are OPR documents for helpdesk? otherwise is it for the people who work by on-calls in your team
    -> 온콜당직자가 본다.

- 헬프데스크 몇명인가?
  - Do you know how many people are in helpdesk?
    -> 모른다. 외부에 있다. 완전 외주다.

---

[기타-프로그램]
- 메신저 프로그램
  - ====> 공식적으로는 스카이프를 씀. 개발팀 프로젝트 파트에 따라서 teams나 slack을 쓰는 파트도 있음



- 디지털오퍼레이션팀(유헬스팀) 옆에서 같이 보면서 배우면 안될까?
  - Can I have my place move to your team? I want to learn how your team works nearby. And I'd like to see what they do and what program they use.

[Digital-Operation]

1. When you deploy new functions to live server from test server, do all modified parts in test deploy to live, otherwise can you select some of them to deploy to live?
  - ====> TN – We have a list of ‘table’s or programs that we can promote or move from our Development server to Production Server.  The list is customized to our own configuration.


2. Before you release new functions, do users also involve in the test? Do they write some test result documents? If it does, can you show me an example?
  - ====> TN – Yes, we involve end users to qualify the new functionality.  Usually this is done thru a project process.  We usually help write the test scripts.  The scenarios information come from the Clinical users or departmental areas.  See attached excel spreadsheet as sample of our test script.


3. Can you send me SOP(Standard Operate Procedure) documents? If it's so big, Can you send me some part of it? Because It would be a helpful reference for our team.
  - ====> Sure, see attached SOP example.


4. Can you give me two more screenshots? The one is the screen of making a new EPR screen. And another one is the screen of a release history page, which is containing request ID.
  - ====> Sure.  See attached document.


<Organization>
1.	Could you explain to me what do people do in each part? 각파트의 사람들이 하는일은?
  ====> 궁금한 부서만 다시 확인해서 물어보기

<HIS>
캡처 - 서비스나우 리퀘스트
EPR - 메인화면


- 서비스 나우에 프로그램 새기능, 수정 요청도 들어오나?
  - Do you receive the requirments about new functions of EPR from Service Now?
    - ====> 아직은 아님. 헬프데스크로 들어오는 이슈건만 받고 있음. 향후에는 서비스 나우로 모두 이관될 예정

- I heard that EPR Facility Merge Project have gone live last week. Do you know how long does it take? whole proejct period? EPR 통합 프로젝트에 걸린기간은?
  - ====> 전체 2년이 걸림.

- What kinds of modules does EPR include? I received EPR FACILITY EMERGE project go-live support documents. Is that all about the EPR modules? 어떤 모듈들로 구성되어 있는지?
  - ====> 메인화면 스크린 샷.. 전체 모듈에 대한 구성도는 없음. 스크린샷을 보고 대충 정리해야할 듯.

A.	Do you have a whole source of EPR? EPR소스를 가지고 있는지?
  - ====> 소스는 없음

H.	How many requirements for modify or add functions are your team receiving from users one month? 한달에 HIS수정 요구사항이 몇건이나 들어오는지?
  - ====> 10~20건정도

- What kinds of languages and framework are used for HIS? 뭘로 개발되어 있는지? 클라이언트/서버 사이드?
  - 알수없음. 패키지라서 관리하지 않는다.

B.	Can I see the architecture diagram of HIS? HIS아키텍처 설계도 볼 수 있을지?
E.	How many instances of HIS is operating? 인스턴스는 몇개 띄워져있는지?
  - ====> 없음

F.	What kinds of vender are you using in WAS and DB? WAS,DB는 어디껄 쓰는지?
  - ====> 업체 자체 솔루션 Cache라는 디비를 씀

C.	How many environments of HIS set in UHN besides live? For example, it's for developing, testing, stagging, educating. HIS 운영외 개발, 테스트, 교육 환경이 있는지?
  - ====> 운영, 개발, 테스트, 교육1,2 있음.

D.	Do you have an environment for High-Availability? 이중화되어있는지?
  - =====> 이중화구성

G.	The digital operation team has about 200 people. Also, I know that UHN is using the Harris system as a HIS. Harris is not an in-house product. However, is it possible to modify the application by the digital operation team? HIS가 솔루션제품인걸 아는데, 수정하는게 가능한지?
  - ====> 솔루션이지만 들어와서 수정을 했고, 커스터마이징이 가능하다. 기능추가 등을 하고 있다.

I.	Is there a clinical decision support system for the doctor? CDSS 기능이 있는지?
  - ====> 없음.

K.	How to make EMR forms? Are there employees in charge of it in the hospital? EMR 서식은 어떻게 만드는지 담당직원이 있는지?
  - ====> 있다.

L.	How to manage screen access authorities of users? 화면권한은 어떻게 관리하는지?
  - ====> EPR에 내재된 기능으로 관리

M.	Do you have policies or rules to protect the patient’s privacy? 환자권한은 어떻게 관리하는지?
  - =====> 환자권한 롤로 우리처럼 디테일하게 관리하지 않는다. 역할에 화면에 대한 권한과 환자에 대한 권한이 약간 섞여 있다.

N.	Is there a session timeout? 세션 타임아웃있는지?
  - ====> 있다. 보통은 10분. 개인공간은 1시간까지 허용한다.

O.	Do you have a single-sign-on function? If you have one, how many systems are connected? SSO를 사용하는지?
  - ====> LDAP을 쓴다. LDAP을 쓰는 시스템끼리 아이디, 패스워드는 동일하게 쓰지만 SSO 는 아니다.

<Software Quality Management>
1.	I’d like to know what kinds of documents you write under the software development life cycle. 설계, 개발 프로세스에서 어떤 문서들을 남기는지?
  - ====> 안남김

2.	Do you have any process for software quality management? For example, do you have the coding rule? Also, do you have a code inspection tool or peer coding process? SW품질관리를 위한 별도의 툴을 사용하는지?
  - =====> Atlassian

3.	Do you do code review regularly? How often do you do a code review? 코드 리뷰같은건 하는지?
  - =====> 아니

4.	Do you have a technical study group or some gatherings? 스터디 그룹같은게 활성화되어 있는지?
  - =====> 아니


<Software Development Life Cycle>
1.	Analysis
  A.	I'd like to see your development process from getting requirements from users to releasing the application. 개발프로세스를 알고 싶다.

  B.	Do you have meetings with end-users to understand their requirements? 엔드유저와의 미팅이 있는지?

  C.	Do you write documents abou  t analyzing user requirements? 사용자요구사항 분석 문서를 남기는지?

2.	Design
  A.	Do you write some design papers, when you develop the application? For example, Use case diagram, DFD, like that. 설계문서는 어떤걸 쓰는지?

  B.	If you write design documents, do you have a tool to draw diagrams? 다이어그램을 그리기 위해 툴을 쓰는게 있는지?

3.	Development
  A.	What are you using source version control software? 소스버전컨트롤 프로그램으로 뭘쓰는지?

  B.	Do you use open source a lot when you develop applications? 개발할때 오픈소스 많이 쓰는지?

  C.	How to interoperate data between HIS and other systems? Is there any application for that? HIS랑 레거시랑 데이터 연계를 어떻게 하는지?

  D.	What kinds of languages do you use mainly? 주로 어떤 랭귀지를 쓰는지?

4.	Testing
  A.	How do you know the impact with related application, when you add some functions to the application? Is there a system or process to check about it? 기능 추가시, 연계 테스트는 어떻게 하는지?

  B.	Do you use automating test software? 테스트 자동화 툴이 있는지?

5.	Maintenance
  A.	What kinds of software are you in charge? Can I see the list about it? 오퍼레이션팀에서 관리하는 프로그램 리스트는?
    - ====> EPR. 나머지는

  B.	Do you have all infrastructures like server, machine in the hospital? 인프라가 전부 병원 안에 있는지?

  C.	There are many people in the infrastructure unit. Is that because people are in charge of different infrastructures every application?

  D.	How do you catch the error in the live system? Is there any monitoring system? 운영시스템의 에러를 어떻게 잡는지/찾는지?

  E.	How often do you deploy or release applications that are operating? 얼마나 자주 배포를 하는지?

  F.	How long does it take time to deploy applications? How long does it take time to restart WAS? 배포하는데 시간은 얼마나 걸리는지?

  G.	In my hospital, IT service team members are always ready to on-call because medical staff are working even though during the holiday. If they have a problem with the HIS, the IT service team has to help them. Because sometimes something emergency comes up. How does your team do that situation? 시스템에 오류가 나서 현업의 문의가 오면 어떻게 대응하는지? 주말에는?

  H.	Is the help desk working 24/7? If you don't do that when users meet an error on holiday, how to support them? 24시간 운영되는 헬프데스크가 있는지?

  I.	What kinds of solutions do you have, and what kinds of applications did you develop in-house? 솔루션 리스트와 인하우스로 개발된 리스트?

  J.	what kinds of mobile services are operating now? 모바일 프로그램은 뭐있는지?

  K.	Is it possible to use the cloud service in the hospital? Do you have any system operating in the cloud now? 클라우드 사용이 가능한지? 사용하는게 있는지?



<about-ESB>
1. What do you in charge of in Digital Opeartions Team? 디지털팀에서 맡은역할은? [로라]
  - ====> ESB 시스템을 관리(Red Hat Fuse)

2. How many systems are communicating with ESB? Can I see the list of those systems? ESB를 통해서 HIS와 연계되는 시스템 종류?[로라]
- ====> EPR과 HL7로 연계하는 건수는 185 건이다.
- 다른 방식의 연계 시스템은 몇건인지 정확히 알수없지만, Diagram을 보면 한눈에 알 수 있을 듯하다.

2. I'd like to know the data integration methodology that you are using. 연계방식이 어떤게 있는지? [로라]
- HL7
- JSON
- REST
- SOAP
- ====> 요것도 Diagram받으면 확인 가능

3. Is there another system to communicate with the external system? EAI솔루션 하나인지? 외부/내부 연계 시스템이 별도로 있는지?[로라]
- ====> 하나만 있음

4. I'd like to see monitoring system of ESB 관리콘솔좀 볼 수 있는지[로라]
  - How do you catch errors?
  - How Does the ESB system notify you of errors?
  - ====> Prometheus - 오픈소스 모니터링 시스템 / 설정값에 따라 메일로 인폼을 줄 수 있음
  - ====> grafanaLabs - 로그 비주얼라이징

6. Is it ok with the system average load? In our case, more and more systems want to communicate with main HIS system. 시스템 부하는 괜찮은지? 부하가 많이 몰리지는 않는지? [로라]
  - ====> 초당 75건까지 피크를 친것을 보여줌. 전체적으로 안정되어 있음.

[eHealth-Innovation]
- 음성처방입력이나, AI기술이 진료에 활용되는 사례가 있을까요?
  - I'm wondering where you are using new technologies in the clinical side. For example, It's making an order by speech or predicting cancer by patient's record history.

- Big데이터나 신기술이 활용되고 있는 사례가 궁금하다.
  - Is there a best practice using your application that is made by new technologies like Big data, AI?


---