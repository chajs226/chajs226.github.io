---
layout: post
title: Quenstions
categories: UHN-PLP
---


#### To, Laura
Hello,

I'm Junseong from Asan Medical Center, Seoul, Korea. I'm participating in the Personal Learning Program at UHN.

I'm interested in the ESB system. I heard that you are in charge of the ESB system. Our hospital also is using the ESB system. Also, this is a important part of our system because many kinds of systems communicate with HIS through ESB. I'd like to know how you operate the ESB system.

Here are some of my questions.

1. How many systems are communicating with ESB? Can I see the list of those systems?
2. I'd like to know the data integration methodology that you are using.
3. Is there another system to communicate with the external system?
4. I'd like to see monitoring system of ESB
  - How do you catch errors?
  - How Does the ESB system notify you of errors?
5. ESB is a very critical system. So I think that it's important to keep availability. Have you experienced in ESB system failure?

Thank you for your time.

Junseong,




#### To, Tony
Hi Tony,
I'm Junseong from Asan Medical Center, Seoul, Korea. I'm participating in the Personal Learning Program at UHN.
So I was able to learn VOC's job from Daniel and Nancy so far. Now, I'd like to learn about the HIS of UHN and the digital operation team furthermore.

I'm interested in maintaining HIS, because our hospital has launched a new HIS this March. I was a member of the project and used to design some common functions such as user management, patient authorization management, interface with legacy systems, etc.

Even though we opened a new system, I think we have some challenging for maintenance. We are spending much time adding new functions to HIS. Sometimes we miss the impact of a new function. Also, we always have to ready to on-call to help clinicians. So I'd like to know how your team operate your HIS.
The attachment is about my questions. I'm sorry for too many questions.

<Organization>
- What do people in Application Engineering part do? What are they in charge of?
  - Do they add new functions to HIS, which is the harris system?
- What are the people's role in the Clinical Application Support part? Do they only help doctors inputting the data?

<Culture>
- Do you do code review regularly? How often do you do a code review?
- Do you have a technical study group or some gatherings?

<Operation/Architecture>
- There are many people in charge of infrastructure. Do you have all infrastructures like servers in the hospital? Don't you use the cloud service? (Is it possible to use the cloud service in the medical industry? Do you have any system operating in the cloud now?)
- How many systems are operated by one person?
- What kinds of softwares are your team in charge of? Can I see the list about it?
- I'd like to see your development process from getting requirements from users to deploy to the application.
- How do you catch the error in the live system? Is there any monitoring system?
- How often do you deploy or release applications that are operating?
- How do you know the impact with related application, when you add some functions to the application? Is there a system or process to check it?
- Do you have any process for software quality management? For example, Do you have the coding rule? Also, Do you have a code inspection tool or peer coding process?
- How long does it take to deploy application? How long is the WAS restart time? (In our case, it took time about 40 minutes)
- Do you have an environment for High-Availability?
- How many instances of HIS is running?
- What kinds of vender are you using in WAS and DB?
- How many environments of HIS set in UHN besides live? For example, it's for developing, testing, stagging, educating.
- In my hospital, IT service team members are always ready to on-call because medical staff are working during the holiday, and if they have a problem with the HIS, the IT service team has to help them. How does your team deal with that situation? Is the help desk working 24/7? If you don't do that when users meet an error on holiday, how does your team support them?

<Development>
- What are you using source version control software?
- What kinds of languages are your team using most?
- What kinds of applications do you have, and what kinds of applications did you develop in-house?
- Do you use open source a lot?
- The digital operation team also has about 200 people. Also, I know that UHN is using harris as a HIS. Harris is not an in-house product. However, is it possible to modify the application by the digital operation team? Also, How many requirements are for one month?
- How to interoperate data between HIS and other systems? Is there any application for that?
- what kinds of mobile services are operating now?
- Do you write some design papers, when you develop the application? For example, Use case diagram, DFD, something like that.

<HIS>
- Is there a clinical decision support system for the doctor?
- How do you make new EMR forms? Are there employees in charge of it in the hospital?
- How do you manage screen access authorities of users?
- Do you have policies or rules to protect the patient's privacy?
- Is there a session timeout?
- Do you have a single-sign-on function? If you have one, how many systems are connected?