# PythonAnywhere 를 이용한 Django 프로젝트 배포

> 완성된 Django 프로젝트를 [PythonAnywhere](https://www.pythonanywhere.com/) 를 활용해 배포할 수 있다.
>
> 우선, 배포할 Django 프로젝트를 Github 저장소에 올려둔 상태여야 한다.



### [1] PythonAnywhere에서 Clone

1. PythonAnywhere 가입

   가입 시 지정한 사용자 아이디가 웹사이트 URL에 포함되므로 주의!

   

2. 상단 **Consoles** 메뉴 클릭

   

3. **Start a new console** 아래 **Bash** 클릭

   

4. 아래와 같이 git clone 수행

   ```shell
   $ git clone [github저장소주소] [pythonanywhere아이디].pythonanywhere.com
   ```





### [2] 가상환경 생성 및 Django 설치

1. 가상환경 생성

   ```shell
   $ mkvirtualenv --python=python3.6 [pythonanywhere아이디].pythonanywhere.com
   ```

   가상환경 생성 시, 자동으로 활성화됨

   

   **참고)** 가상환경 활성화하기

   ```shell
   $ workon [pythonanywhere닉네임].pythonanywhere.com
   ```

   

2. 가상환경이 활성화된 상태에서 Django 설치

   ```shell
   $ pip install 'django'
   ```

   

3. Django 초기설정

   ```shell
   $ python manage.py migrate
   ```

   ```shell
   $ python manage.py createsuperuser
   ```

   

   **참고)** 이미 존재하는 admin 아이디를 지우고  싶을 때

   https://m.blog.naver.com/PostView.nhn?blogId=virapasas&logNo=221045166942&proxyReferer=https:%2F%2Fwww.google.com%2F

   

   

### [3] PythonAnywhere에서 웹 생성하기

1. 상단 **Web** 메뉴 클릭

   

2. **Add a new web app** 클릭 후 프로젝트 생성

   * Python > Django 선택

   * 프로젝트 이름이나 경로는 임의로 지정해도 무관하다.

   

3. **Code** 내 /var/...wsgi.py 수정

   ```shell
   import os
   import sys
   
   path = '/home/[PythonAnywhere아이디]/[PythonAnywhere아이디].pythonanywhere.com'
   if path not in sys.path:
       sys.path.append(path)
   
   os.environ['DJANGO_SETTINGS_MODULE'] = '[생성한프로젝트명].settings'
   
   from django.core.wsgi import get_wsgi_application
   application = get_wsgi_application()
   ```

   

   **주의)** `[생성한프로젝트명]` 은 2번 **Add a new app 진행 시 설정한 이름**임!



4. **Virtualenv** 에 가상환경 설치된 주소 입력

   보통 아래 주소에 생성되어 있을 거임

   `/home/[PythonAnywhere아이디]/.virtualenvs/[PythonAnywhere아이디].pythonanywhere.com`

   

5. **Static files** 에서 static과 media 경로 설정

   기존 경로 대신 아래 두 경로로 대체한다.

   * URL:  `/static/`

     Directory:  `/home/[PythonAnywhere아이디]/[PythonAnywhere아이디].pythonanywhere.com/static`

   * URL:  `/media/`

     Directory:  `/home/[PythonAnywhere아이디]/[PythonAnywhere아이디].pythonanywhere.com/media`

   

   위는 경로 지정만 해놓은 것이고, 아래 [4]번 방식을 통해 static 경로에 실제 static 파일을 모아놓아야 한다.



### [4] static 파일 가져오기

1. 상단 **Files** 탭에서 `[PythonAnywhere아이디].pythonanywhere.com` 로 이동해 `settings.py ` 클릭

   

2. static과 media의 경로 지정

   ```python
   STATIC_ROOT = '/home/[PythonAnywhere아이디]/[PythonAnywhere아이디].pythonanywhere.com/static'
   ```

   ```python
   MEDIA_ROOT = '/home/[PythonAnywhere아이디]/[PythonAnywhere아이디].pythonanywhere.com/media'
   ```

   

3. 상단 **Save** 클릭

   

4. 상단 **Console** 메뉴에서 다시 Bash 실행

   

5. 가상환경 활성화 후 clone 해왔던 Django 프로젝트로 이동

   ```shell
   $ workon [pythonanywhere닉네임].pythonanywhere.com
   $ cd /home/[PythonAnywhere아이디]/[PythonAnywhere아이디].pythonanywhere.com/
   ```

   

6. static 파일들을  `settings.py` 에 지정한 경로에 모아주기 위해 아래 명령 실행

   ```shell
   $ python manage.py collectstatic
   ```

   

   **참고)** collect 수행 시 이름이 같은 파일이 있을 때, 한 파일만 모아지게 되므로 주의! 

   만약 static 내에 서로 다른 이름의 폴더에 들어있는 파일이면 이름이 같아도 괜찮다.





### [5] 배포 완료!

실제로 주소를 입력해 웹이 정상적으로 나오고 있는지 확인!

`[PythonAnywhere아이디].pythonanywhere.com/`





### 



