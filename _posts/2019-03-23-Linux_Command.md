---
layout: posts
title: "리눅스 명령어 연습"
categories: [OSS, Linux]
---

OSS 수업에서 리눅스 명령어들을 연습하고 블로그에 포스팅하라는 과제가 나왔습니다.

그런 이유로 이 글에서는 쓸모있을 것 같은 리눅스 명령어들을 간단한 사용법과 함께 적어보고자 합니다.



1) cd (change directory)

말 그대로 현재 디렉토리를 바꾸는 명령어
 
```c
cd /
```
-> 최상위 디렉토리로 이동
```c
cd ...
```
 -> 상위 디렉토리로 이동
```c
cd
```
 -> 홈 디렉토리로 이동

사용 예시)

![cd](https://github.com/woduseh/woduseh.github.io/blob/master/assets/img/1.cd_example.PNG)



2) mkdir (make directory)

디렉토리를 새로 만드는 명령어

```c
mkdir folder
```
 -> 현재 경로에 folder라는 이름의 디렉토리를 새로 생성함
 


3) rm (remove)
 
파일/디렉토리를 제거하는 명령어

```c
rm hello.txt
```
 -> hello.txt라는 파일을 삭제함
 
 
 
4) rmdir (remove directory)

빈 디렉토리를 제거하는 명령어. 디렉토리가 비어있지 않다면 제거할 수 없다

```c
rmdir folder
```
--> folder 라는 빈 디렉토리를 삭제함



5) mv (move)

파일이나 디렉토리를 이동하거나, 이름을 변경할 때 사용하는 명령어

```c
mv folder1 folder2
```
 -> folder1의 이름을 folder2로 변경함
 
```c
mv folder1 /lower_directory
```
 -> folder1이라는 디렉토리를 현재 디렉토리 안에 있는 lower_directory라는 디렉토리 안으로 이동시킴
 


6)
