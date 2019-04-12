---
layout: posts
title: "Git&Github 기초"
categories: [OSS, Git]
---

#### Git과 Github 기초 사용법
---



- Git이란? 분산 버전 관리 툴

- Github란?  깃(Git)을 사용하는 프로젝트를 지원하는 웹호스팅 서비스

- Repositiory - 저장소

- Fork - 사본 생성. 즉, UNIX의 fork()처럼 원본 프로젝트를 복사해와서 내 원격 저장소에 저장함

- Clone - 내 원격 저장소에 있는 내용을 로컬 저장소로 복사

- add, commit... - 개발작업 로컬 반영

- Push - 로컬 저장소에서 수정한 내용들을 내 원격 저장소에 붙여넣음

- Pull - 내 원격 저장소에 있는 내용들을 원본 프로젝트에 추가함

- PR: pull request - 내가 commit한 파일을 원본에 추가해주길 request함



일반적으로 fork -> clone -> 개발 (add, commit...) -> push -> pull request -> pull (원본 소유자가 pull을 한다면) 으로 진행된다

예시) (2019-04-09 OSS 강의내용)

7주차 - PR 해보기 순서
1. GitHub에 로그인 한 후, 이곳의 Repository를 fork 합니다.
1. 자신의 GitHub 페이지에 같은 이름으로 Repository가 만들어졌는지 확인
1. peace에 로그인 한 후, oss2019 디랙토리에서 자신의 위 Repository를 다운로드(clone)합니다.
```
git clone https://github.com/자기계정/oss2019spring
```
1. vim 으로 다음과 같은 파일을 만들고 내용을 입력합니다.
```
1.  파일이름은 반드시 자신의 이름.txt 로 할 것.  
1.  파일 내용에는 첫번째 줄에는 자신을 한 줄의 문장으로 소개합니다.  
1.  두번째 줄에는 이 수업을 6주동안 들으면서 느낀 소감을 한줄로 표현합니다.  
1.  세번째 줄에는 본인이 느끼는 최근 과제의 난이도를 1(아주쉬움) ~ 10(아주어려움) 사이의 실수값으로 적습니다.  
```
1. 다음의 순서대로 작업한 파일을 commit & push 하세요
```
1.  git add <위에서만든파일명>
1.  git commit -m "OOO의 첫번째 PR을 보냅니다!"  
1.  git push    
```
1. 자신의 GitHub 페이지에 방금 올린 파일이 제대로 있는지 확인
1. Pull Request 보내기 (상단 Pull request 탭)
```
1.  New pull request 클릭  
1.  Create pull request 클릭

1. Pull Request 보내지고, 받아들여졌는지 확인
```



- merge: PR을 받아들일지 말지 결정하여 받아들이기로 판단했을 때 받아들이는 행위
 - 주의점) 기존 파일과 이름이 같을 경우, 
 
 
참고 : MD 문법 https://heropy.blog/2017/09/30/markdown/
