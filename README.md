# codyssey-my-own-room
Codyssey - 개발 환경 구축 및 실습 기록

1. 프로젝트 소개

본 프로젝트는 코디세이 과정의 개발 환경 구축 미션을 수행하며 Linux CLI, Docker, Git 및 GitHub의 기본적인 사용 방법을 학습하고 실습한 기록입니다.

단순히 명령어를 실행하는 것에 그치지 않고, 각 도구의 작동 원리와 사용 목적을 이해하고 실제 실행 결과를 확인하는 것을 목표로 합니다.

2. 개발 환경

항목

환경

OS

Windows 11

Linux

Ubuntu (WSL)

개발 도구

Visual Studio Code

Container

Docker

Docker Engine

29.9.3

Version Control

Git

Repository

GitHub

3. 필수 미션 수행 내역

Mission 1. Linux CLI 기초

pwd, ls, cd를 이용한 경로 및 디렉터리 확인

mkdir, touch를 이용한 디렉터리와 파일 생성

cat을 이용한 파일 내용 확인

cp, mv, rm을 이용한 파일 복사, 이동 및 삭제

chmod를 이용한 파일 권한 변경

Mission 2. Docker 기초

Docker Engine 버전 및 작동 상태 확인

Docker 이미지 다운로드 및 확인

컨테이너 생성, 실행, 중지 및 재시작

docker exec와 컨테이너 내부 접속 실습

Dockerfile 작성 및 이미지 빌드

Nginx 컨테이너 실행

포트 매핑을 이용한 웹 서버 접근

Mission 3. Docker 데이터 관리

Bind Mount를 이용한 호스트와 컨테이너 간 파일 공유

Volume 생성 및 연결

컨테이너 삭제 후 데이터 유지 여부 확인

컨테이너 재시작을 통한 데이터 지속성 확인

Mission 4. Git 및 GitHub

Git 사용자 설정 확인

Git 저장소 연결

VS Code와 GitHub 연동

변경 사항의 add, commit, push 실습

GitHub 원격 저장소에 결과물 업로드

4. 검증 명령어

docker --version
docker info
docker images
docker ps -a
docker logs codyssey-web
docker stats --no-stream
docker volume ls
docker volume inspect nginx-data

git status
git branch --show-current
git remote -v
git config --get user.name

5. 프로젝트 파일 구조

ia-codyssey/
├── README.md
├── cli-practice/
│   └── basic/
│       └── hello.txt
├── docker-practice/
│   ├── Dockerfile
│   └── html/
│       └── index.html
└── screenshots/
    ├── 01_docker-ps.png
    ├── 02_dockerfile.png
    ├── 03_bind-mount.png
    ├── 04_volume.png
    └── 05_vscode-github.png

6. 스크린샷 및 실습 증거

파일명

내용

01_docker-ps.png

Docker 컨테이너 실행 상태

02_dockerfile.png

Dockerfile 작성 및 확인

03_bind-mount.png

Bind Mount 실습

04_volume.png

Docker Volume 실습

05_vscode-github.png

VS Code 및 GitHub 연동

7. 트러블슈팅

문제 1. GitHub 저장소 접근 오류

비공개 저장소를 Clone하는 과정에서 저장소를 찾을 수 없다는 오류가 발생했습니다.

저장소의 공개 여부와 GitHub 계정 인증을 확인한 뒤 정상적으로 연결했습니다.

문제 2. Linux 파일 경로 오류

파일 권한 변경 실습 중 대상 파일이 존재하지 않는다는 오류가 발생했습니다.

현재 Ubuntu 홈 디렉터리에 실습 폴더가 없는 것을 확인하고 mkdir -p 명령어로 폴더를 생성한 후 파일을 다시 만들어 해결했습니다.

8. 추가 미션

추가 미션 수행 결과는 별도 항목으로 기록할 예정입니다.

9. 마무리

이번 미션을 통해 개발 환경을 구성하는 과정부터 컨테이너 실행, 데이터 관리, 버전 관리까지 직접 경험했습니다.

처음에는 익숙하지 않은 명령어와 환경 설정으로 어려움이 있었지만, 오류를 확인하고 해결하는 과정을 통해 개발 도구의 기본적인 사용 방법을 익힐 수 있었습니다.

앞으로도 각 기술의 사용법뿐 아니라 작동 원리까지 이해하는 것을 목표로 학습을 이어가겠습니다.

Repository: https://github.com/junhwilim1022/ia-codyssey
