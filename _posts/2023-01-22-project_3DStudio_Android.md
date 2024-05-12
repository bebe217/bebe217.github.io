---
layout: post
title: Urbanbase 3D Studio Android / 어반베이스
date: 2023-01-22 23:18 +0800
last_modified_at: 2023-10-19 01:08:25 +0800
tags: [프로젝트, 포트폴리오, Android, AR, 3D]
toc: false
---


Urbanbase 3D Studio Tablet Android QA 대응 및 추가 기능 개발

> 자사 Asset들로 여러 도면에서 3D 인테리어를 해볼 수 있는 앱

***

iOS 초기 배포 이후, 아직 미완성 기능이 남아 배포하지 못한 안드로이드 사이드에 자발적으로 넘어가 배포까지 도와 개발하였습니다. 얼마 뒤 안드로이드 리드개발자의 퇴사로 인해 폐업시 까지 안드로이드 사이드에서 잔여 QA들과 추가 기능들을 개발하였습니다.
iOS개발 당시 Unity협업은 팀장님이 도맡아 해서 경험해 보지 못해 아쉬운 점이 있었는데 1인칭 시점 개선안을 적용하며 짧은 시간이나마 3D팀과의 협업을 해 볼 수 있었습니다.

### 담당업무
- 3D Studio Android QA 대응
- 3D Studio Android 추가 기능 개발
   - 1인칭 시점 진입 시나리오 개선 
     - 탑뷰 이동 및 시점 선택 추가
     - 가이드 화면 추가
   - 지도 현재 위치 포커싱 기능 추가

### 기술스택

- Kotlin, Google Map, 자사 ARViewer SDK, Unity(3D팀 사이드)

- Bitbucket, Jira, Firebase App Distribution
  
***

### 주요 화면



1인칭 시점 플로우 개선
<iframe width="560" height="315" src="https://www.youtube.com/embed/zrIe2YoI2FU" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

현위치 기능 추가
<img width="100%" src="https://lh3.googleusercontent.com/u/0/drive-viewer/AKGpihYhxmr90ddM5fec5gH3GhCEcYackVEYGqIOzrwRJiIGgm99itBX-4oWp_5pW2hCt3-tyVXG2sXHMbFjr_4m_0JWEIlMwquUjG0=w3420-h1846-rw-v1">