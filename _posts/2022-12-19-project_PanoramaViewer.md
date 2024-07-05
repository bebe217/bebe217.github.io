---
layout: post
title: PanoramaViewer / 어반베이스
date: 2022-12-19 23:18 +0800
last_modified_at: 2022-01-19 01:08:25 +0800
tags: [프로젝트, 포트폴리오, iOS, WebKit]
toc: false
---


전시회용 PanoramaViewer iPad 개발

> 기존 웹 파노라마 뷰어를 iPad에서 전체화면으로 보여주는 앱

***

도면 리스트에 해당하는 기존 자사 웹 파노라마 주소를 웹뷰로 말은 앱입니다.<br>
사업개발팀 막내분과 전시회에 대해 의논하다 적은 공수에 비해 보기 좋은 결과물이 나올 것 같아 적극적으로 나서서 개발해 드렸습니다.<br>
엑셀로 넘겨 받은 제공 도면목록은 Firebase Remote Config 넣어 앱에서 받을 수 있게 가볍게 구현하였습니다.
화면은 디자인 없이 기존 자사 앱 디자인과 유사하게 보이도록 만들었습니다.<br>
동탄 설치 이후에는 반응이 좋았는지 다른 박람회에도 앱을 사용하였는데, 인터넷 상황이 좋지 않은 박람회에 쓸 수 있도록 프론트팀에서 각 도면의 파노라마 뷰 코드 파일을 넘겨 받아 앱에 심어 띄우는 offline 앱도 개발하였습니다.
  
### 담당업무
- 도면 리스트
- 웹뷰에 파노라마 뷰어 연결

### 기술스택

- Swift, WebKit, 자사 웹 파노라마 뷰어

- Firebase Remote Config, App Distribution
  
***

### 주요 화면

전시회 공간
<img width="100%" src="/assets/images/9f02972b8ccddcf5b29dccf0b9d62871.jpg">

<iframe width="560" height="315" src="https://www.youtube.com/embed/cdt_vAbbIZA" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

