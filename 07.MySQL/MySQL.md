# MySQL

## 기본 명령어

### 접속

```shell
mysql -u root -p
```

어떤 디렉토리에서 입력해도 상관 없음



### 전체 데이터베이스 조회

```mysql
show databases;
```



### 특정 데이터베이스 사용하기

```mysql
use [데이터베이스명]
```

`(none)` 이 사용하는 데이터베이스 이름으로 바뀜



### 테이블 조회

```mysql
use [데이터베이스명];
```



### 새로운 데이터베이스 생성

```mysql
CREATE database [데이터베이스명]
```

생성 후 `show databases;` 입력해 정상적으로 만들어졌는지 확인



### 새로운 사용자 계정 만들기 

```mysql
CREATE USER "scott"@"localhost" IDENTIFIED BY "tiger"
```

* `scott`은 계정이름
* `tiger`는 비밀번호



### 사용자에게 권한 부여

```mysql
GRANT ALL PRIVILEGES ON [데이터베이스명].* to "scott"@"localhost";
```

```mysql
FLUSH PRIVILEGES;
```





### MySQL 종료

```shell
quit
```

또는 `Ctrl + C`

