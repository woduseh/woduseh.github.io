---
layout: posts
title: "Web Hosting"
categories: [OSS, Ubuntu, Web]
---
# Ubuntu Apt 명령어 설명

- apt-get [option]
  - update: 패키지 목록을 갱신
  - install [패키지 이름]: 패키지 설치
  - upgrade: 설치되어 있는 모든 패키지를 새 버전으로 업그레이드
  - autoremove [패키지 이름]: [패키지 이름]에 의존성이 있어서 [패키지 이름]이 없으면 필요없는 다른 패키지까지 전부 다 삭제
  - remove [패키지 이름]: 패키지 삭제 (설정 파일은 지우지 않음)
  - purge [패키지 이름]: 패키지 삭제 (설정 파일까지 모두 삭제)
- apt-catch [option]
  - stats: 기본적인 통계들을 보여줌
  - pkgnames: 시스템에 설치된 모든 패키지 이름들의 리스트를 출력
  - search [패키지 이름]: 패키지 검색
  - show [패키지 이름]: 패키지 정보 보기
---
# 여러가지 웹호스팅의 기초

### Php 설치하기
1. ```sudo apt install php php-mysql``` 명령어를 통해 php 설치
![설치방법](https://woduseh.github.io/assets/images/php1.PNG)
2. ```$ sudo nano /var/www/html/info.php``` 명령어를 통해 info 파일을 편집기로 열어서 ```<?php phpinfo(); ?>``` 를 입력
3. 웹 브라우저를 켜고 localhost/info.php 에 접속하여 확인

결과: ![php ](https://woduseh.github.io/assets/images/PHPINFO.PNG)


### Mysql 설치하고 mysqld가 시작되었는지 확인하기
1. ```sudo apt install mysql-server``` 명령어를 통해 mysql 서버 패키지 설치
2. Mysql 세팅

```
webnautes@webnautes-pc:~$ sudo mysql_secure_installation

Securing the MySQL server deployment.

Connecting to MySQL using a blank password.

VALIDATE PASSWORD PLUGIN can be used to test passwords
and improve security. It checks the strength of password
and allows the users to set only those passwords which are
secure enough. Would you like to setup VALIDATE PASSWORD plugin?

Press y|Y for Yes, any other key for No: y

There are three levels of password validation policy:

LOW    Length >= 8
MEDIUM Length >= 8, numeric, mixed case, and special characters
STRONG Length >= 8, numeric, mixed case, special characters and dictionary                  file

Please enter 0 = LOW, 1 = MEDIUM and 2 = STRONG: 1
Please set the password for root here.

New password:   root 패스워드를 입력합니다.

Re-enter new password: 

Estimated strength of the password: 50 
Do you wish to continue with the password provided?(Press y|Y for Yes, any other key for No) : y
By default, a MySQL installation has an anonymous user,
allowing anyone to log into MySQL without having to have
a user account created for them. This is intended only for
testing, and to make the installation go a bit smoother.
You should remove them before moving into a production
environment.



데이터베이스를 아무나 읽어볼 수 없게 합니다.
Remove anonymous users? (Press y|Y for Yes, any other key for No) : y
Success.
```

3. DB를 새로 생성하고 DB를 사용할 사용자도 새로 생성한 뒤 사용자에게 DB를 사용할 권한을 부여

결과: ![mysql 결과](https://woduseh.github.io/assets/images/Mysql.PNG)

### phpmyadmin을 설치하고 브라우저로 확인
1. ```sudo apt install phpmyadmin``` 명령어로 phpmyadmin을 설치
2. 설치 설정창에서 apache2 -> 예 를 입력한 뒤 암호 설정

결과: ![phpmyadmin 결과](https://woduseh.github.io/assets/images/Phpmyadmin.PNG)

### apache 서버를 상태확인/시작/중지/재시작하기
상태 확인: service apache2 status
시작: service apache2 start
중지: service apache2 stop
재시작: service apache2 restart

### 홈 디렉터리 변경해 보기 (/var/www/html/ —> 특정계정/html/) 
1. 터미널을 켜고 ```sudo nano /etc/apache2/apache2.conf``` 명령어를 실행하여 아파치 설정 파일을 켠다
2. apache2.conf 파일에서 아래 <Directory /> 부분을 찾아서 루트디렉토리로 사용할 위치를 기록한다
3. ```sudo nano /etc/apache2/sites-available/000-default.conf``` 를 통해 아파치 웹서버의 사이트 설정파일을 수정한다. (000-default.conf 파일수정)
4. 아파치 웹서버 중지 후 재시작

### DB 계정 만들어 wordpress 간단 설치 및 확인
1. 워드프레스용 DB를 생성하고 DB에 사용자 계정 연결
2. 
```
sudo apt update
sudo apt install php-curl php-gd php-intl php-mbstring php-soap php-xml php-xmlrpc php-zip

```
으로 여러 유용한 php 익스텐션들 설치
3. 
```
1.특정 계정의 홈디렉터리 가동 체크 및 해당 디렉토리로 이동
2.최신 워드프레스 설치용 압축파일 다운로드 $ wget https://wordpress.org/latest.tar.gz
3.압축풀기 $ tar –xvzf lastest.tar.gz
4.압축파일 삭제
```
4. 워드프레스 설정 파일 세팅
```
1. wp-config.php 파일에 들어가서 아까 만든 DB 이름, DB 유저, DB 비밀번호를 입력한다
2. 추가적으로 보안을 위해 'AUTH_KEY' 들의 값을 변경할 수도 있다
```
5. 웹사이트에 접속하여 워드프레스 설치 진행

결과: ![워드프레스 결과](https://woduseh.github.io/assets/images/wordpress.PNG)

---
# 웹 호스팅 Virtual Host 세팅 방법 찾아보기 
1. ```sudo vi /etc/apache2/sites-available/000-default.conf``` 을 통해 설정파일 접속
2. ```Listen 을 통해 새로운 포트를 열고 새로운 포트에 대한 설정을 마침```
3. 위에 올린 것처럼 새로운 계정에 워드프레스 새로 설치
4. 포트 번호를 바꿔가며 워드프레스 확인

---
참고 자료: 
```
https://blog.outsider.ne.kr/346
https://www.manualfactory.net/10175
https://ngee.tistory.com/128
// Apt 명령어 설명

https://webnautes.tistory.com/1185 // php, mysql, phpmyadmin 설치 설명

https://zetawiki.com/wiki/%EC%95%84%ED%8C%8C%EC%B9%98_%EC%9B%B9%EC%84%9C%EB%B2%84 // 아파치 서버 관련 명령어 설명

https://m.blog.naver.com/yexx/220720241912
https://m.blog.naver.com/cjwdark/220617377179
https://blog.xianchoi.kr/268
// 아파치 웹서버 홈 디렉토리 변경 설명

https://antilibrary.org/1884
https://ko.wordpress.org/txt-install/
https://jimnong.tistory.com/746
https://webdir.tistory.com/210
// wordpress 설치 설명

https://mygumi.tistory.com/64 
https://webdir.tistory.com/213
// 가상 호스트 설정 설명
```
