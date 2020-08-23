# CLI

## `GUI` vs. `CLI`

> GUI: Graphic User Interface
>
> CLI: Command Line Interface



## 기초 명령어

### (1) `pwd`

* print working directory

* 현재 폴더의 경로를 알려줌

  ```shell
  $ pwd
  ```

* 기본 경로를 home directory 라고 함

### (2) `ls`

* list: 현재 폴더 내 디렉토리 보여줌

### (3) `cd [폴더명]`

* change directory
* 폴더를 변경

### (4) `cd ..`

* 상위폴더로 이동

### (5) `mkdir`

* 새 디렉토리(폴더) 생성
* 삭제는 `rmdir`

### (6) `touch [파일명]`

* (비어있는) 파일을 생성

* 들어갈땐 

  ```shell
  $ vi hello.txt
  ```

### (7) `echo [출력내용]` 

* 화면 출력 (print)

  ```shell
  $ echo 'ggg'
  ```

### (8) `cp [복사할 파일명] [새로운 파일명]`

* copy: 파일 또는 폴더 복사

### (9) `rm [파일명]`

* remove: 파일 또는 폴더 삭제

### (10) `cp -r [복사할 폴더명/] [새로운 폴더명/]`

* `-r` : recursive 의 약자

* 삭제는 `rm`

  ```shell
  $ rm -r new/
  ```

### (11) `mv [타겟파일(경로)] [이동할 폴더]`

* move: 파일 (또는 폴더) 이동 & **이름 변경**

  ```shell
  $ mv ~/Desktop/00_markdown_basig.md .
  ```

  **참고)** 

  * `.` : 현재 위치
  * `~` : home directory



**참고)** 정상적으로 설치되어 있는지 확인할 때; 버전 확인

```shell
$ git --version
```