# Python 가상환경

## [1] PYTHON

1. 가상환경 만들기

   ```shell
   python -m venv [가상환경이름]
   ```

   프로젝트 안에 가상환경을 만들 때, 보통 `.venv` 라는 이름으로 생성함

   

2. 가상환경 활성화

   ```shell
   cd [가상환경폴더 경로]/Scripts/activate.bat
   ```

   



## [2] Anaconda

1. 가상환경 만들기

   ```shell
   conda create -n [가상환경이름] python=[설치버전]
   ```

   

2. 가상환경 활성화

   ```shell
   activate [가상환경이름]
   ```



3. 가상환경 비활성화

   ```shell
   deactivate [가상환경이름]
   ```

   

4. 다른 패키지에 저장된 패키지 정보 가져와서 일괄 설치하기

* 가상환경에 설치된 패키지 정보 저장

  ```shell
  conda list -n [가상환경이름] --export > [파일저장할경로]\[파일명].txt
  ```

  

  json 형식으로도 내보내기 가능

  ```shell
  conda list -n [가상환경이름] --json > [파일저장할경로]\[파일명].json
  ```

  

* 저장된 패키지 정보에 있는 패키지 일괄 설치

  설치할 가상환경을 활성화(activate)한 상태에서 아래 명령어 실행

  ```shell
  conda install --file [경로\패키지정보 저장된 파일명].txt
  ```

  (json이라면 형식을 json으로만 바꿔서 실행!)

  

* 가상환경 생성과 패키지 설치를 동시에 처리할 수도 있다

  ```shell
  conda create -n [가상환경이름] --file [경로\패키지정보 저장된 파일명].txt
  ```

  

5. 생성되어 있는 가상환경 전부 조회

   ```shell
   conda env list
   ```



6. 활성화되어 있는 가상환경 내 설치된 패키지 전부 조회

   ```shell list
   conda list
   ```

   

7. 특정 가상환경 삭제

   ```shell
   conda remove -n [가상환경이름] --all
   ```

   