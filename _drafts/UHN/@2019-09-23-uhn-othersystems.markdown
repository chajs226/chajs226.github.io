---
layout: post
title: Orientation
categories: UHN-PLP
---

# ESB
- Red Hat FUSE 시스템 사용. 레드햇의 지원을 받고 있음
- 정확히는 모른다. HL7 데이터 연계만 185개를 하고 있다.

  - EPR - ESB -(ADT) - LOB,PCS,NODR 등등 3개로 카운트
- internal, external 모두 ESB 하나의 시스템이 담당하고 있음.
- DB to DB 방식의 연계는 쓰지 않음. single transaction으로만 씀. 서비스 메시지 시스템의 형식임.
- PROMETHUES (오픈소스)
  - 메시지 로우 파일을 모으는 시스템
  - 시간이 오래걸리는 메시지등을 필터를 걸어서 확인 가능
  - ESB와는 별도의 메시지를 모으는 시스템
  - 이메일로 담당자에게 noti를 줌
- GRAFANALABS (오픈소스)
  - PROMETHUES에서 모은 데이터를 비주얼라이징해주는 시스템

Esb 디비안쓰는 이유. 표준화된 통신방식의 방향으로 가야된다. 오픈서비스...
에이전트는 내부간의 통신방식이고, 연계시스템의 확장에 많은 제한이 따른다. 내부간의 보안, 안정성만 담보된다면 굳이 Agent를 설치하고할 필요가 있을까?

