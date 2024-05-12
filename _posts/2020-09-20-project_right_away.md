---
layout: post
title: 오늘당장 / 콜링그룹
date: 2018-07-09 23:18 +0800
last_modified_at: 2019-09-29 01:08:25 +0800
tags: [프로젝트, 포트폴리오, 안드로이드]
toc:  false
---

오늘당장 안드로이드 앱 개발

> 사용자와 사용자 사이의 서비스 중개 어플리케이션

<img width="200px" src="/assets/images/right_away.png" style="border-radius:5%">
사용자 간의 서비스를 중개하는 어플리케이션으로 해주세요, 해드려요, 오늘마켓으로 구분되며 각각 서비스 의뢰, 서비스 제공 및 마켓 화면으로 이루어져 있습니다.<br>
갓 생긴 스타트업에서 신입 한분과 함께 작업을 했기 때문에 평소 개발해 보고 싶은 방식대로 개발해 볼 수 있었습니다.<br>
안드로이드에서 당시 비교적 최근에 나온 DataBinding, LiveData, ViewModel, Constraintlayout 등을 이용해 개발을 하였으며, 디자이너가 원하는 UI가 있으면 커스텀뷰를 이용해 최대한 구현하였습니다.
<br class="clearer" />

***

### 담당업무
안드로이드 개발 담당(Java)
- 서비스 목록, 서비스 화면, 입찰 기능, 글쓰기 화면, 알림, 댓글, 리뷰 등의 화면 개발
- 전체적인 앱 구조 설계
- 재사용 가능한 UI 구현
- 사진 라이브러리(uCrop) 커스터마이징
- 아임포트 연동
- 채팅창 구현 등

### 기술스택

- Java, MVVM, Retrofit, Glide, uCrop
  
- Bitbucket, Notion, Zeplin

***

### 주요 화면

<sub>* 폐업하여 스토어 링크가 없습니다. 퇴사 시 apk와 코드도 두고 와서 디자인 이미지로 개발 내용을 서술합니다.</sub>
<br>
<br>

#### 서비스 리스트

<img src="/assets/images/190927_ask_list.jpg">

사용자들이 올린 서비스들이 보여지는 화면입니다.
<br>홈 화면에서는 하단 네비게이션 안에 상단 탭 또한 존재하여 초반에 전체적인 틀을 잡는 데에 공을 들였습니다. 모두 프래그먼트로 구현하면 구조가 복잡해질 것 같아, 각 네비게이션 항목은 액티비티로 구현하고 상단 탭 항목만 프래그먼트로 구현해 앱 관리를 용이하게 하였습니다.
<br>디자이너의 요청대로 스크롤다운할 시에 상단 탭이 아이콘만 사라지고 글자만 남도록 CoordinatorLayout을 통해 구현하였습니다. 상단 탭이 바뀔 때마다 화면 전체의 색상 테마가 변경되는 UI라, 탭 변경 이벤트가 올 때마다 색상 변경을 해주었습니다.

<br class="clearer" />

#### 서비스 상세화면

<img src="/assets/images/190927_ask_writer_detail.jpg">
서비스 요청 상세보기 화면입니다. 해당 화면의 세부 부분은 다른 곳에 사용되는 부분도 많아 사용자, 사진뷰페이저, 댓글, 수행비 제안 등 재사용이 가능한 부분을 따로따로 커스텀 뷰로 만들어 사용하였습니다.

<br class="clearer" />
<img src="/assets/images/190927_ask_bid.jpg" style="float=right">

지도는 웹뷰로, 각 수행 위치별 좌표 정보를 url에 쏴주어 프론트단에서 만든 지도 화면을 불러왔습니다.<br>
제안자 내역은 횡스트롤 리스트로, 제안자 선택 상태에 따라 하단 버튼이 변경됩니다. 노란 아이콘 클릭 시 제안자가 작성자에게 작성한 글이 팝업으로 뜨도록 구현하였습니다. 해당 사용자를 클릭 시에 새로운 액티비티로 해당 사용자 정보를 보여줍니다.

<br class="clearer" />

#### 글쓰기

<img src="/assets/images/190927_writing_additional.jpg">

하나의 액티비티에서 프래그먼트로 단계를 이동합니다. 하나의 뷰모델에 정보를 저장하고 이전을 누를 시 뷰모델에 담긴 정보를 데이터바인딩으로 뿌려줍니다.<br>
추가 요청은 커스텀뷰로 계속 추가, 삭제할 수 있습니다.

<br class="clearer" />
<img src="/assets/images/190927_writing_help_end.jpg">

사진등록 부분을 클릭 시 갤러리로 넘어가고, 앱의 모든 사진은 정사각형 규격으로 정했기 때문에, 갤러리에서 선택된 사진을 uCrop 라이브러리로 불러와 사용자가 원하는 부분을 1:1 크기로 자릅니다. uCrop 라이브러리는 테마색상 변경이나 기능 제거, 타이틀 변경 정도를 수정하였습니다.

<br class="clearer" />
<img src="/assets/images/190927_writing_help_loc.jpg">

상위 항목 선택 시, 하위 항목이 뿌려지는 형태이며 동은 세 개까지 선택 가능하게 구현하였습니다.

<br class="clearer" />

#### 내 정보

<img src="/assets/images/190927_myprofile.jpg">

하단 바 상단의 영역을 프래그먼트로 구성하였으며, 항목 선택 시 왼쪽으로 슬라이딩 되는 모션으로 프래그먼트를 이동시켰습니다.

<br class="clearer" />

#### 리뷰

<img src="/assets/images/h-2_system_situation_popup.jpg">
<img src="/assets/images/190927_history_review.jpg">

평점 모양은 공통 커스텀 뷰로 만들어, 평점주기 화면은 터치 이벤트를 받아 구현하였으며 평점 보여주기로 타입을 줄 시 터치 이벤트를 막았습니다.

<br class="clearer" />

#### 메세지

<img src="/assets/images/190927_message_list.jpg">

프로필 사진은 CircleImageView 라이브러리를 썼으며, 새 메세지 표시는 커스텀뷰를 만들어 사용하였습니다.

<br class="clearer" />

<img src="/assets/images/190927_message_chat_default.jpg">
<img src="/assets/images/h-2_system_message.jpg">

채팅이 앱의 주된 기능이 아니었고 서버측에서 간단히 구현하기를 원하였기에 소켓통신을 쓰지 않고 일반 Rest Api 형식으로 구현하였습니다.

<br class="clearer" />

#### bottom sheet

<img src="/assets/images/190927_suggestion.jpg">
<img src="/assets/images/190927_myhistory_ask_filter.png">

만들었던 하단 팝업들입니다.

<br class="clearer" />

***

### 결과

자금 문제로 인한 회사 폐업으로 1차 알파버전에서 프로젝트가 중단되었습니다. 1년 동안 타 부서의 사람들과 토의하며 만든 하나의 서비스가 런칭을 못하고 사라져서 아쉬운 프로젝트 였습니다.
또한 익숙한 자바로 빠르게 1차 버전 릴리즈 후 차차 코틀린으로 변경을 계획했지만, 초기버전이라 여러 기획 변경으로 1차 버전의 개발 기간이 길어지고 런칭이 불발되어 코틀린 사용을 하지 못했던 점 또한 아쉬운 점으로 남아있습니다.

<br class="clearer" />