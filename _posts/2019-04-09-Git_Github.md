---
layout: posts
title: "Git&Github 기초"
categories: [OSS, Git]
---

Git과 Github 기초 사용법

Git이란? 분산 버전 관리 툴

Github란?  깃(Git)을 사용하는 프로젝트를 지원하는 웹호스팅 서비스

Repositiory - 저장소

Fork - 사본 생성. 즉, UNIX의 fork()처럼 원본 프로젝트를 복사해와서 내 원격 저장소에 저장함

Clone - 내 원격 저장소에 있는 내용을 로컬 저장소로 복사

add, commit... - 개발작업 로컬 반영

Push - 로컬 저장소에서 수정한 내용들을 내 원격 저장소에 붙여넣음

Pull - 내 원격 저장소에 있는 내용들을 원본 프로젝트에 추가함

PR: pull request - 내가 commit한 파일을 원본에 추가해주길 request함



일반적으로 fork -> clone -> 개발 (add, commit...) -> push -> pull request -> pull (원본 소유자가 pull을 한다면) 으로 진행된다
