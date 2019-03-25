---
layout: posts
title: "리눅스 명령어 연습"
categories: [OSS, Linux]
---

OSS 수업에서 리눅스 명령어들을 연습하고 블로그에 포스팅하라는 과제가 나왔습니다.

그런 이유로 이 글에서는 쓸모있을 것 같은 리눅스 명령어들을 간단한 사용법과 함께 적어보고자 합니다.



1) cd (change directory)

현재 디렉토리를 바꾸는 명령어
 
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
mkdir [생성하려는 디렉토리 이름]
```
 -> 현재 경로에 [생성하려는 디렉토리 이름]이라는 이름의 디렉토리를 새로 생성함

사용 예시)

![example_mkdir](https://woduseh.github.io/assets/images/example2.PNG)

3) rm (remove)
 
파일/디렉토리를 제거하는 명령어

```c
rm [제거할 파일 이름/디렉토리 이름]
```
 -> [제거할 파일 이름/디렉토리 이름]이라는 파일/디렉토리를 제거함
 
사용 예시)

![example_rm](https://woduseh.github.io/assets/images/example3.PNG)
 
4) rmdir (remove directory)

빈 디렉토리를 제거하는 명령어. 다만 디렉토리가 비어있지 않다면 제거할 수 없다

```c
rmdir [제거할 빈 디렉토리 이름]
```
--> [제거할 빈 디렉토리 이름] 라는 빈 디렉토리를 삭제함
 
사용 예시)

![example_rmdir](https://woduseh.github.io/assets/images/example4.PNG)

5) mv (move)

파일이나 디렉토리를 이동하거나, 이름을 변경할 때 사용하는 명령어

```c
mv [바꾸기 전 디렉토리 이름] [바꾼 후 디렉토리 이름]
```
 -> [바꾸기 전 디렉토리 이름]의 이름을 [바꾼 후 디렉토리 이름]으로 변경함
 
```c
mv [상위 디렉토리] [하위 디렉토리]
```
 -> [상위 디렉토리]라는 디렉토리를 현재 디렉토리 안에 있는 [하위 디렉토리]라는 디렉토리 안으로 이동시킴
 
 상위에서 하위로 가는 것 뿐만이 아니라 하위에서 상위로 가거나 하는 것도 자유롭다
 
사용 예시)

![example_mv](https://woduseh.github.io/assets/images/example5.PNG)

6) cat

파일의 내용을 출력하는 명령어. 파일에 내용을 입력할 때도 사용할 수 있다
```c
cat [출력하려는 파일 이름]
```
 -> [출력하려는파일 이름]의 내용을 출력한다
 
```c
cat > [내용을 입력하려는 파일 이름]
```
 --> [내용을 입력하려는 파일 이름]에 내용을 입력할 수 있게 된다. 입력모드에서 나오려면 ctrl+d를 누르면 된다
  
사용 예시)

![example_cat](https://woduseh.github.io/assets/images/example6.PNG)

7) ls (list directory contents)

현재 디렉토리의 내용 목록을 출력
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
chmod 755 [권한을 설정하려는 파일/디렉토리 이름]
```
 -> [권한을 설정하려는 파일/디렉토리 이름]의 사용권한을 rwxr-xr-x로 설정
 
(좌측부터 순서대로 소유자 - 그룹 - 모든 사용자이며 r=4, w=2, x=1. 755의 의미는 소유자는 rwx, 그룹은 r-x, 모든 사용자는 r-x)

사용 예시)

![example-chmod](https://woduseh.github.io/assets/images/example8.PNG)

9) clear

터미널 화면을 비우는 명령어

```c
clear
```
 -> 현재 화면에 출력된 것을 모두 비운다
 
사용 예시)

![example-clear](https://woduseh.github.io/assets/images/example9.PNG)

10) cp (copy)

파일/디렉토리을 복사하는 명령어

```c
cp [복사하려는 파일/디렉토리 이름] [복사될 파일/디렉토리 이름]
```
 -> [복사하려는 파일/디렉토리 이름]라는 파일/디렉토리를 복사해서 [복사될 파일/디렉토리 이름]라는 이름을 붙임
 
사용 예시)

![example-cp](https://woduseh.github.io/assets/images/example10.PNG)

11) pwd (print working directory)

현재 디렉토리를 프린트하는 명령어

```c
pwd
```
 -> 현재 디렉토리를 출력한다
 
사용 예시)

![example-pwd](https://woduseh.github.io/assets/images/example11.PNG)

12) logout

로그인 셸에서 로그아웃

```c
logout
```
 -> 프로그램 종료
 
사용 예시)

![example-logout](https://woduseh.github.io/assets/images/example12.PNG)


13) ln

링크를 생성하는 명령어

```c
ln [링크를 생성하려는 파일 이름] [링크될 파일 이름]
```
 -> 하드 링크 생성 ([링크를 생성하려는 파일 이름] [링크될 파일 이름]은 서로 같은 파일을 가르킨다. 그래서 하드 링크가 걸린 파일을 지우려면 두 파일을 다 지워야한다)
 
```c
ln -s [링크를 생성하려는 파일 이름] [링크될 파일 이름]
```
 -> 심볼릭 링크 생성 (윈도우의 바로가기와 같다고 생각하면 된다. 하드 링크와 마찬가지로 둘 중 어느것만 수정해도 둘 다 수정된다)
 
사용 예시)

![example-ln](https://woduseh.github.io/assets/images/example13.PNG)



14) date

현재 날짜와 시간을 출력하는 명령어

```c
date
```
 -> 현재 날짜와 시간을 출력한다
 
사용 예시)

![example-date](https://woduseh.github.io/assets/images/example14.PNG)



15) du (disk usage)

디렉토리의 용량을 출력하는 명령어

```c
du
```
 -> 현재 디렉토리 내 디렉토리와 폴더들의 용량을 출력한다
 
사용 예시)

![example-du](https://woduseh.github.io/assets/images/example15.PNG)



16) locale

로케일 정보를 조회하는 명령어

```c
locale
```
 -> 현재 로케일 정보를 출력한다
 
사용 예시)

![example-locale](https://woduseh.github.io/assets/images/example16.PNG)



17) man (manual)

메뉴얼을 출력하는 명령어

```c
man [명령어]
```
 -> [명령어] 를 사용하는 방법이 담긴 메뉴얼을 출력한다
 
사용 예시)

![example-man](https://woduseh.github.io/assets/images/example17.PNG)



18) shutdown

리눅스를 종료하는 명령어

```c
shutdown -h [시간값]
```
 -> [시간값] 만큼의 시간이 지나면 리눅스를 종료한다 
 
사용 예시)

![example-shutdown](https://woduseh.github.io/assets/images/example18.PNG)



19) kill

프로세스를 강제로 종료하는 명령어

```c
kill [종료할 프로세스 ID]
```
 -> [종료할 프로세스 ID]를 종료한다
 
사용 예시)

(실행중인 프로세스가 없어서 종료하지 못했다만 이런 방식으로 사용하면 된다...)
![example-kill](https://woduseh.github.io/assets/images/example19.PNG)



20) passwd

패스워드를 변경하는 명령어

```c
passwd
New password: [변경할 비밀번호]
Retype new password: [변경할 비밀번호]
```
 -> [변경할 비밀번호]로 비밀번호를 변경한다
 
사용 예시)

(비밀번호를 바꾸고 싶지 않기에 일부러 이렇게 실행했으나 사용법대로 실행하면 비밀번호가 바뀐다)
![example-passwd](https://woduseh.github.io/assets/images/example20.PNG)



21) who

현재 서버에 로그인한 사용자를 모두 출력하는 명령어

```c
who
```
 -> 현재 서버에 로그인한 사용자를 모두 출력한다
 
사용 예시)

![example-who](https://woduseh.github.io/assets/images/example21.PNG)



22) whoami

현재 로그인한 내 자신의 계정을 출력하는 명령어

```c
who
```
 -> 현재 서버에 로그인한 내 자신의 계정을 출력한다
 
사용 예시)

![example-whoami](https://woduseh.github.io/assets/images/example22.PNG)



23) echo

뒤이어 입력되는 문자열을 모니터에 출력하는 명령어

```c
echo [출력하려는 문자열]
```
 -> [출력하려는 문자열]을 모니터에 출력한다
 
사용 예시)

![example-echo](https://woduseh.github.io/assets/images/example23.PNG)



24) env

시스템 환경변수를 출력하는 명령어

```c
env
```
 -> [출력하려는 문자열]을 모니터에 출력한다
 
사용 예시)

![example-env](https://woduseh.github.io/assets/images/example24.PNG)



25) ps

시스템에서 실행되고 있는 프로세스 목록을 출력하는 명령어

```c
ps
```
 -> 시스템에서 실행되고 있는 프로세스 목록을 출력한다
 
사용 예시)

![example-ps](https://woduseh.github.io/assets/images/example25.PNG)



26) find

파일/디렉토리를 검색하는 명령어 

```c
find [찾으려는 키워드]
```
 -> 현재 디렉토리 기준으로 찾으려는 키워드가 어디에 있는지 출력한다
 
사용 예시)

![example-find](https://woduseh.github.io/assets/images/example26.PNG)



27) locate

파일/디렉토리를 검색하는 명령어

```c
locate [찾으려는 키워드]
```
 -> 찾으려는 키워드가 어디에 있는지 그 절대경로를 출력한다
 
사용 예시)

![example-locate](https://woduseh.github.io/assets/images/example27.PNG)



28) tree

디렉토리 목록을 트리구조로 보여주는 명령어

```c
tree
```
 -> 디렉토리 목록을 트리구조로 출력한다
 
사용 예시)

![example-tree](https://woduseh.github.io/assets/images/example28.PNG)



29) more

cat과 비슷하게 파일을 출력하는 명령어

```c
more [출력하려는 파일]
```
 -> [출력하려는 파일]을 출력한다
 
사용 예시)

![example-more](https://woduseh.github.io/assets/images/example29.PNG)



30) which

명령어가 저장된 위치를 출력하는 명령어

```c
which [찾으려는 명령어]
```
 -> [찾으려는 명령어]가 저장된 위치를 출력한다
 
사용 예시)

![example-which](https://woduseh.github.io/assets/images/example30.PNG)




앞으로도 계속 추가할 예정입니다.
