---
layout: post
title: Urbanbase 3D Studio iOS / 어반베이스
date: 2022-07-22 23:18 +0800
last_modified_at: 2023-01-19 01:08:25 +0800
tags: [프로젝트, 포트폴리오, iOS, AR, 3D]
toc: false
---


Urbanbase 3D Studio Tablet iOS 신규 개발

>  기존에 웹으로 서비스증인 3D 인테리어 서비스를 태블릿 앱으로 신규개발

***

기존 회사의 대표 프로덕트인 웹 3D 인테리어 서비스를 태블릿 버전으로 개발하였습니다.
회사의 동탄 전시회 기한에 맞추어 빠른 개발이 필요했기에 동료들과 잦은 야근 및 주말 출근을 하며 함께 멋진 결과물을 만들어 내어 뿌듯한 프로젝트 중 하나이지만 런칭 후 1년도 되지 않아 앱스토어에서 내려가게 되어 많은 아쉬움이 있습니다.
각종 인테리어 관련 작업은 3D팀에서 Unity로 만들어 빌드결과물을 앱에 넣고 3D팀에서 뚫어준 api를 통해 여러 기능을 사용하게 만들었습니다.

### 담당업무
- 3D Studio iOS 신규 개발
  - 홈 및 메뉴 레이아웃 화면 구성 (expandable)
  - 회원가입 및 로그인 개발
  - 기업별 스튜디오 전환 및 유저 기능 전반 개발
    - 기업, 일반 회원 구분
    - 국가별 서비스 구분
    - 일반 계정에서 여러 스튜디오 이동할 수 있게 구현
    - 스튜디오 별 사용가능 서비스 분기
  - 지도 전반 기능 개발
    - 좌표별 마커 및 클러스터링
    - 건물 검색 및 상세 정보
  - 도면 전반 기능 개발
  - 스타일링(에디터X) 전반 기능 개발
  - 프로필 및 설정 개발
  - 빌드 config 설정
- UBGear (iOS) 개발
  GraphQL은 아니지만 회사 api가 비슷한 방식을 차용해 클라이언트단에서 필요한 기능을 쿼리로 작성해 요청하는데,
  쿼리문을 쉽게 작성 할 수 있게 만든 모듈
  - 전반 기능 담당

### 기술스택

- Swift, StoryBoard, Google Map, 자사 ARViewer SDK, Unity(3D팀 사이드)

- Bitbucket, Jira, Figma, Firebase App Distribution
  
***

### 주요 화면


앱스토어 화면
<img width="100%" src="/assets/images/studiostore.png">

기업별 스튜디오 선택화면
<img width="100%" src="/assets/images/select_studio.png">

로그인
<iframe width="560" height="315" src="https://www.youtube.com/embed/_TkLprw2BEM" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

앱 기능 전반
<iframe width="560" height="315" src="https://www.youtube.com/embed/qRP7gMUwWlk" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

지도 기능 전반
<iframe width="560" height="315" src="https://www.youtube.com/embed/9VQgF7nb2YQ" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

지도 검색
<iframe width="560" height="315" src="https://www.youtube.com/embed/MXtUyLbNqHs" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

스타일링 에디터 (제가 개발한 부분은 아닙니다)
<iframe width="560" height="315" src="https://www.youtube.com/embed/grntLc6vDpU" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>