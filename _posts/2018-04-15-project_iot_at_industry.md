---
layout: post
title: IoT@Industry / (주)LG유플러스
date: 2016-04-15 23:18 +0800
last_modified_at: 2018-04-20 01:08:25 +0800
tags: [프로젝트, 포트폴리오, 안드로이드]
toc: false
---


IoT@Industry 통합 사용자앱 개발

> 공장 출입감지 및 앱 접근 제한 산업 IoT 어플리케이션

산업 IoT 어플리케이션으로 공장 소속 직원이 이 앱을 통해서만 다른 공장 관련 어플리케이션에 접속할 수 있습니다. 공장 관련 어플리케이션에 접속하려면 공장 전용망에 접속해야 하는데, 공장 진입 시 비콘 감지를 통해 자동으로 망전환 됩니다. 공장 밖으로 이동 시, 비콘이나 ECGI 변경을 감지해 일반 통신망으로 전환시켜 공장 관련 앱들에 접근할 수 없게 합니다.

***

### 담당업무

첫 직장에서 처음으로 맡았던 프로젝트(Android)이자 마지막으로 맡았던 프로젝트(iOS)입니다. 신입시절에는 주로 보조로 개발하였으며, IoT에 대한 전반적인 체험을 할 수 있는 좋은 기회였습니다.<br>
마지막으로 맡은 iOS 신규 개발건에서는 거의 혼자서 개발을 맡게 되었는데, iOS 개발은 처음이었지만 개발 투입을 위해 빠른 Swift공부와, Codable 등 나름 iOS에서는 그 당시 최근에 나온 기술들을 써보려고 노력하였습니다.

안드로이드 개발(Java)
- UI구현
- 원스토어 연동
- 삼성 자급제폰에 대해 Knox api 적용
  - AdminReceiver등록 및 knox 키 인증
  - knox api로 망변경 기능 추가
- 망변경 로직 수정
- 테더링 제어 기능 추가

iOS 신규 개발(Swift)
- StoryBoard로 UI구성, auto-layout 화면 구현
- Location Manager 구현 (서버에서 받은 좌표로 사용자 진입 시 알림)
- iOS MDM, Configuration Profile 설치 구현
- 전화번호 인증 웹뷰 화면 구현
- 다국어 적용
  
### 기술스택

- Java, Swift

- Svn, Trello, Excel
  
***

### 주요 화면
<br>
<img width="50%" src="/assets/images/iot_industry_screenshot.png">
화면은 거의 웹뷰로 구성하여 UI쪽 보다는 백그라운드에서 통신망 변경 감지 및 비콘 감지 기능이 주가 된 어플리케이션입니다.<br>
목록에 보이는 앱들은 고객 전용망에 접속 시에만 활성화되며, 공장 외부에서는 접근 불가하기에 사용자의 출입을 감지해 망변경을 시켜 접근을 제한합니다.<br>
또한 목록에 있는 앱은 다른 회사에서 개발한 앱들인데, 타 회사와 공통 규격을 맞추어 사용자의 상태를 공유하였습니다.

<br class="clearer" />

### 까다로웠던 부분
iOS에서 MDM 관련 profile 설치 쪽이 자료가 별로 없어 개발이 까다로웠으나, 타 프로젝트에서 먼저 개발해 보았던 직원의 도움으로 개발을 잘 마무리할 수 있었습니다.<br>
공장 출입 시마다 profile 설치 및 제거가 빈번하였기 때문에 서버 측에서 매번 프로파일 요청하는 방식을 원하지 않아서 서버에서 최초 1번 사용자에 해당하는 profile을 받아 파일로 저장해 두고 설치 시 GCDWebServer 라이브러리를 이용해 profile을 띄워 사파리로 설치하였습니다.

### 결과
[원스토어 링크](https://m.onestore.co.kr/mobilepoc/apps/appsDetail.omp?prodId=0000700935)

<br class="clearer" />