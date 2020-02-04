# ainci-tizen
> AinCI-Tizen creates Build, Test, and CI servers with Docker to automatically generate system images for porting to Tizen-based IoT devices. This provides a development server infrastructure for Tizen-based IoT devices.

> AinCI-Tizen는 Tizen-based IoT 장비들을 포팅하기 위한 시스템 이미지를 자동으로 만들기 위해 필요한 빌드, 테스트, CI 환경을 서버에 docker를 사용하여 만들어준다.

## 통합된 솔루션

> nginx/php7.3 가상 호스팅, proxy 솔루션
>  - Tizen 이미지 관리 솔루션 지원

> OpenProject 프로젝트 관리 솔루션

> Jenkins CI 솔루션

> Tizen 빌드 솔루션



* 통합 예정 솔루션

> git server

> docker-image server

* DB는 데이터의 안정성을 위해 Docker로 제공하지 않으며 따로 설치하여 사용 하기를 권장함
* Tizen 이미지 관리 솔루션은 3306 포트가 local과 포트포워딩 되어 있으므로 이를 통해 외부 서버와 연동 가능함

## 서비스 특징

> [OpenProject] : 프로젝트 관리 프로세스(PMI)를 지원 하는 오픈 소스 프로젝트 관리 소프트웨어

> [Jenkins] : CI 툴 중 하나로 CI (Continuous Integration)는 개발자가 공유 버전 제어 저장소에서 
  팀의 코드를 컴파일 할 수 있도록함으로써 빌드주기 비 효율성을 줄이기 위한 프로세스

> [nginx-vhost-php7.3] 기반의 가상 호스팅, OpenProject, Jenkins를 개별 서버로 사용할 수 있고 
  단일 nginx에 통합하여 사용할 수 있음

> 예) test.com 도메인을 통해 a.test.com/ b.test/com 으로 가상 호스팅을 운영하고 
      open.test.com으로 오픈프로젝트를 운영,
      jen.test.com으로 jenkins를 운영할 수 있음

> [Tizen-Builder-Env] : 설명 추가

> 상위 솔루션은 compose/full_service 안의 docker-compose.yml 파일을 실행하여 
  하나의 nginx 컨테이너를 통해 각각 다른 도메인으로 서비스를 연결할 수 있음

## 사용 방법 

가상 호스팅 사용 방법 : [nginx-vhost-php7.3]

OpenProject, Jenkins 사용 방법 : [nginx-vhost_php7.3_openproject_jenkins_docker-image]

Tizen-Builder 구축 방법 

```sh
docker-compose up -d
```

Jenkins와 Tizen-Builder 연동 방법

```sh
docker-compose up -d
```

Tizen 이미지 관리 솔루션 연동 방법

```sh
docker-compose up -d
```


## 사용 예제

스크린 샷과 코드 예제를 통해 사용 방법을 자세히 설명합니다.
- 업데이트 예정

## 개발 환경 설정

만약 Docker 설치와 Docker-compose 설치가 되어 있지 않다면 다음 사항을 확인함

> docker 설치 참고 사이트 [docker-install]  
> docker-compose는 apt-get을 통해 설치가 가능한 것으로 확인됨

## 업데이트 내역

* 0.0.1
    * 안정화 작업 중

## 멤버

임도현 Owner S/W, H/W, 개발자/기획자

임태연 Member 디자이너/마케터

강동훈 Member S/W, H/W, 개발자/연구원

<!-- Markdown link & img dfn's -->
[nginx-vhost-php7.3]: https://github.com/bluebamus/nginx-vhost-php7.3
[nginx-vhost_php7.3_openproject_jenkins_docker-image]: https://github.com/bluebamus/nginx-vhost_php7.3_openproject_jenkins_docker-image
[OpenProject]: http://wiki.webnori.com/display/pms/Open+Project+7
[Jenkins]: https://jjeongil.tistory.com/810
[Tizen-Builder-Env]: 
