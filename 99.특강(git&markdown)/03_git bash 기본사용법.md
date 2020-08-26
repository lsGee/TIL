# 기본 개념

$ git init 시....

(master) git으로 관리되는 폴더라는 일종의 마크..!

$ ls -a 시...

숨겨진 폴더(.git) 볼 수 있게 됨



1. git 은 폴더 단위로 파일을 관리
2. 관리 관련 내용은 .git/ 폴더에 존재함
3. git 상태를 저장이 곧 commit 이다.
4. git을 SCM(Source Code Management), VCS(version Control System)이라 부름





## Add & Commit

1. stage(index) 위에 파일/폴더 올린다

   ```shell
   $ git add 00_markdown_basic.md
   ```

   	* 사진찍을 준비 끝남! (`$git status` 시 확인 가능) ; 이때의 warning 은 무시...!
	* 폴더 안 모든 파일 갖고 오고 싶으면 `.` !!!
   

   
2. 사진 찍어서 보관! -> 하나의 버전 (commit)

   

3. 찍은 사람 정보(메타데이터)와 함께 커밋시킨당

   ```shell
   $ git commit -m "first commit"
   ```

4. 기록 내역은 아래와 같이!

   ```shell
   $ git log
   ```

   만약 마지막 버전 하나만 보고 싶다면 아래와 같이...!

   ```shell
   $ git log --oneline -1
   ```

5. 다시 상태 확인 `$ git status`

   

6. (추가) 변경된 내용 확인하려면?

   ```shell
   $ git diff [--staged]
   ```

   

7. 특정 시점 버전 확인(만) 하러 갈 때

   ```shell
   $ git checkout [버전 코드]
   ```

   다시 master(현재)로 돌아가려면? 버전 코드 부분에 master!

   

8. 깃허브에 올릴 주소와 원격저장소 지정?

   ```shell
   $ git remote add [원격저장소이름] [깃허브저장소url]
   ```

   **참고)** 원격 저장소 이름은 'origin'으로 쓰는 관례가 있음

   주소 잘 적었나 확인할 땐 아래 명령어로!

   ```shell
   $ git remote -v
   ```

   

9. push해주기

   ```shell
   $ git push [원격저장소이름] [master]
   ```



**[요약]**

> git init
>
> (+ git status)
>
> git add
>
> git commit
>
> git log
>
> git push



## clone

1. **처음** 받아올 때 (repository 정보 없을 때)

   ```shell
   $ git clone [github URL]
   ```

2. (작업 후) 다시 push하기

   ```shell
   $ git push origin master
   ```

   url 정보나 원격저장소 이름 등은 이미 github에 저장되어 있기 때문에 쓸 필요 X

3. **2번째** 받아올 때 (이미 repository 정보 있을 때 = 추가된 버전만 받아올 때)

   ```shell
   $ git pull origin master
   ```

   -> `git log`로 버전 확인~

<hr>



## SHELL에서 Code 창 열기

```shell
$ code [경로]
```

**참고)** 현재 경로는 `.` !!!



## GitHub pages

* repository 만들 때, 이름 설정 : `[유저이름].github.io`
* `[유저이름].github.io` 사이트 접속 시 `README.md` 혹은 `index.html` 노출



## Git을 활용한 협업

1. Push & Pull : 초대가 필요
2. Fork & Pull Request : 오픈소스(초대가 필요 없다)
   * pull request : 수정한 코드 반영해달라고 다시 원작자에게 요청
3. Shared Repository (현업!)
   * Git Flow
   * Github Flow



## branch

현재 존재하는 branch들을 조회

1. `git branch [브랜치명]` 

   처음 생기는 주인 브랜치가 `master`

2. `git branch`

   모든 브랜치 확인

3. `git checkout [브랜치명]`

   특정 브랜치로 이동

4. `git branch -d [브랜치명]`

   비어 있는 특정 브랜치 삭제

5. `git branch -D [브랜치명]`

   비어있지 않은/병합되지 않은 브랜치 삭제

6. `git merge [브랜치명]`

   브랜치를 병합(merge) -> 해당 명령어는 받아올 브랜치(ex. master)에서 써줘야 함

   > 브랜치는 1회용이다. 때문에 한 번 merge했으면 해당 branch를 지워주고 가야 함

7. PR 에서 commit 완료되고 나서 다시 git에서 pull할 때, master에서 pull!



## 취소
1. add 취소
    * 전체 취소
    ```shell
    git reset
    ```
    * 특정 파일 취소
    ```shell
    git reset HEAD [파일명]
    ```

2. commit 취소
    * 가장 최근 1개 commit 취소
    ```shell
    git reset HEAD^
    ```
    `^`의 개수에 따라 최근 n개 commit 삭제 가능
