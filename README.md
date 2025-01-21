# Visual Studio Code에서 컴파일을 위한 gcc컴파일러 설정방법

## Mingw 설치와 환경 변수 경로 설정

1. 다음 주소에서 Mingw를 설치한다.
https://sourceforge.net/projects/mingw/

2. Mingw설치중, 설치 설정창이 뜨면 모두 체크를 눌러 설치를 마친다.

3. 설치 후, 윈도우 시작 창에서 '시스템 환경 변수 편집'을 검색해 '시스템 속성'창을 연다.

4. '시스템 속성'창에서, '환경 변수'를 클릭해 '환경 변수' 창을 연다.

5. '시스템 변수'에서, 'Path'를 클릭 후 '편집'을 클릭하여 '환경 변수 편집'창을 연다.

6. '새로 만들기'를 클릭하여 **경로를 설정** 후, '확인'을 클릭하여 편집을 마친다.

   6 - 1. 설치된 Mingw 폴더에 들어가 보면 많은 실행파일이 담겨있는 bin폴더를 확인할 수 있다. 이 bin폴더의 경로를 복사한다. 

   6 - 2. bin의 경로를 '새로 만들기를 클릭하여 붙여넣고, '확인'을 클릭하여 편집을 마친다. 

7. cmd를 열어 "gcc --version" 명령어를 입력한다. Mingw의 버전 정보가 표시되면 성공이다.


## tasks.json / launch.json설정

1. Visual Studio Code를 실행하여 원하는 폴더를 연다.

2. '.vscode'파일에서, 'tasks.json'파일을 만들어, [다음 내용](https://github.com/BaeGakKyeong/setting-gcc-for-VScode/blob/main/tasks.json, "tasks.json")을 복사해 붙여넣는다.

3. '.vscode'파일에서, 'launch.json'파일을 만들어, [다음 내용](https://github.com/BaeGakKyeong/setting-gcc-for-VScode/blob/main/launch.json, "launch.json")을 복사해 붙여넣는다.

4. 'control + shift + b'로 빌드하여, 컴파일러가 동작하는지 확인한다.


## 빌드된 실행파일 실행하기

1. 'name.c' 파일을 빌드하여 'name.exe'파일이 생성됨을 확인한다.

2. VScode 터미널에 "name.exe"(cmd가 아닌 Windows PowerShell을 사용하고 있다면, 대신 ".\name.exe"명령어를 입력할 것.)명령어를 입력하여, 실행파일이 실행됨을 확인한다.


## 실행파일 실행 자동화

1. '.vscode'파일에서, 'tasks.json'파일을 열고, [다음 내용](https://github.com/BaeGakKyeong/setting-gcc-for-VScode/blob/main/launch(build%20and%20run).json, "tasks(build and run).json")을 복사해 붙여넣는다.

2. 'control + shift + b'로 빌드하고 실행하여, 수정한 'tasks.json'파일이 제대로 동작하는지 확인한다.
