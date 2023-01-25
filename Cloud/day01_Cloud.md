# Day 02

## -- Cloud --

### ▷ Docker

1. 도커의 구조와 특징

- 도커(Docker)
  - 애플리케이션을 **개발/배포/실행**하기 위한 플랫폼
  - 컨테이너를 사용하여 애플리케이션 및 지원 구성 요소 개발
  - 성능 손실을 최소화 
- 도커 엔진과 도커 데몬(dockerd)
  - Docker 객체와 서비스들을 관리
  - 도커 데몬 - 도커 프로세스가 실행되어 입력 받을 준비가 된 상태
- 도커 클라이언트(docker)
  - 명령어를 Docker API 형태로 도커 데몬에게 전달
- 도커 레지스트리(Registry)
  - 이미지들을 저장하고 공유해주는 원격 저장소



2. 도커 이미지 관리하기

- 도커 이미지

  - 컨테이너를 만들고 실행하기 위한 읽기 전용 파일(템플릿)
  - 모든 컨테이너는 이미지 기반으로 생성

- 도커 이미지와 컨테이너

  - 컨테이너는 필요한 파일과 설정을 이미지에서 읽기전용으로 가져다 사용
  - 변경된 사항만 컨테이너 계층에 별도 저장
  - 하나의 이미지로 여러 컨테이너에서 사용가능

- 도커 허브(Docker Hub)

  - 중앙 이미지 저장소
  - 도커 계정 있으면 누구나 이미지 업로드/다운로드 가능
  - 기본적인 리눅스 운영체제부터 웹서버, 데이터베이스, 각종 애플리케이션 등의 다양한 종류의 이미지를 도커 레지스트리에서 내려 받아 컨테이너로 생성

- 도커 이미지 이름

  - **[저장소이름/]이미지이름[:태그]**
    - 저장소 이름 생략 -> 도커 허브 공식 이미지로 인식
    - 태그는 버전을 나타냄
    - 태그 생략 -> 최신 버전으로 인식

- 이미지 검색

  - docker search <키워드>

- 이미지 다운로드

  - docker pull [저장소이름/]<이미지이름>[:태그]

- 이미지 목록 조회

  - docker images

- 이미지 세부정보 조회

  - docker image inspect \<IMAGE ID>

- 이미지 추출

  - 도커 이미지를 별도의 파일로 저장할 때 사용
    - docker save -o <파일명> <이미지명>[:태그]
      - -o : 추출될 파일명을 지정
  - 추출된 파일을 다시 도커 내 이미지로 로드
    - docker load -i <파일명> 
      - -i  : 로드할 파일명을 지정

  
