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

![example_cd](https://woduseh.github.io/assets/images/example1.PNG)

2) mkdir (make directory)

디렉토리를 새로 만드는 명령어

```c
mkdir folder
```
 -> 현재 경로에 folder라는 이름의 디렉토리를 새로 생성함

사용 예시)

![example_mkdir](https://woduseh.github.io/assets/images/example2.PNG)

3) rm (remove)
 
파일/디렉토리를 제거하는 명령어

```c
rm hello.txt
```
 -> hello.txt라는 파일을 삭제함
 
사용 예시)

![example_rm](https://woduseh.github.io/assets/images/example3.PNG)
 
4) rmdir (remove directory)

빈 디렉토리를 제거하는 명령어. 디렉토리가 비어있지 않다면 제거할 수 없다

```c
rmdir folder
```
--> folder 라는 빈 디렉토리를 삭제함
 
사용 예시)

![example_rmdir](https://woduseh.github.io/assets/images/example4.PNG)

5) mv (move)

파일이나 디렉토리를 이동하거나, 이름을 변경할 때 사용하는 명령어

```c
mv folder1 folder2
```
 -> folder1의 이름을 folder2로 변경함
 
```c
mv folder1 lower_directory
```
 -> folder1이라는 디렉토리를 현재 디렉토리 안에 있는 lower_directory라는 디렉토리 안으로 이동시킴
 
사용 예시)

![example_mv](https://woduseh.github.io/assets/images/example5.PNG)

6) cat

파일의 내용을 출력하는 명령어. 파일에 내용을 입력할 때도 사용할 수 있다
```c
cat hello.txt
```
 -> hello.txt 의 내용을 출력한다
 
```c
cat > a.txt
```
 --> a.txt에 내용을 입력할 수 있게 된다. 입력모드에서 나오려면 ctrl+d를 누르면 된다
  
사용 예시)

![example_cat](https://woduseh.github.io/assets/images/example6.PNG)

7) ls (list directory contents)

현재 디렉토리의 내용 목록을 출력한다
```c
ls
```
 -> 현재 디렉토리에 있는 숨기지 않은 모든 파일, 디렉토리의 목록을 출력한다
 
```c
ls -a
```
 -> 현재 디렉토리에 있는 숨겨진 파일, 디렉토리를 포함한 모든 파일, 디렉토리의 목록을 출력한다

```c
ls -l
```
 -> 현재 디렉토리에 있는 모든 파일, 디렉토리의 목록을 접근 권한과 함께 출력한다
 
사용 예시)

![example_ls](https://woduseh.github.io/assets/images/example7.PNG)

8) chomd (change mode)

파일 또는 디렉토리의 접근권한을 변경하는 명령어

```c
chmod 755 folder
```
 -> folder의 사용권한을 rwxr-xr-x로 설정
(좌측부터 순서대로 소유자 - 그룹 - 모든 사용자이며 r=4, w=2, x=1. 755의 의미는 소유자는 rwx, 그룹은 r-x, 모든 사용자는 r-x)

사용 예시)

![example_chmod](https://woduseh.github.io/assets/images/example8.png)

9) clear

터미널 화면을 비우는 명령어

```c
clear
```
 -> 현재 화면에 출력된 것을 모두 비운다
 
사용 예시)

![example_clear](https://woduseh.github.io/assets/images/example9.png)

10) cp (copy)

파일/디렉토리을 복사하는 명령어

```c
cp name.txt name2.txt
```
 -> name.txt라는 파일을 복사해서 name2.txt라는 이름을 붙임
 
사용 예시)

![example_cp](https://woduseh.github.io/assets/images/example10.png)

11)



12)



13)



14)



15)



16)



17)



18)



19)



20)



21)



22)



23)



24)



25)



26)



27)



28)



29)



30)



앞으로도 계속 추가할 예정입니다.
