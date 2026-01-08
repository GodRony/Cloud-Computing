# 클라우드 컴퓨팅 백엔드 파트 코드 


## AWS를 이용한 블로그 사이트 구축


<img width="363" height="248" alt="image" src="https://github.com/user-attachments/assets/783aee73-c0d8-4ea2-824d-d649f7aa9a86" />


### 1. 목적

AWS 학습 및 응용을 위한 프로젝트입니다.


### 2. 특징

기존 로컬 환경에서는 Node.js와 PostgreSQL로 구현됨


EC2 내 nginx, Node.js, PostgreSQL, git, certbot 사용


Node.js와 PostgreSQL 이용 서버 구동


PM2 추가 설치하여 무중단 서비스 제공


### 3. 버전 정보

- OS: Ubuntu 24.04
- 인스턴스 유형: t2.micro (프리 티어에서 사용 가능)
- 보안 그룹: HTTPS (443), SSH (22) 허용
- 키 페어(pem)는 조원 간 공유

### 4. 사용한 기술 정리

**4.1 PostgreSQL**


<img width="497" height="462" alt="image" src="https://github.com/user-attachments/assets/f0b4a5ef-25a0-48d5-8dfe-b4fed01eabd9" />

데이터베이스 시스템.  AWS RDS를 거치지 않고 AWS의 EC2와 직접 연결

**4.2 Node js**

자바스크립트로 서버 애플리케이션 구현

**4.3 certbox**

 특정 도메인에 대한 인증서를 발급

**4.4 Node js**

Node js 보조


### 5. 구조

<img width="787" height="463" alt="image" src="https://github.com/user-attachments/assets/d54b7419-30aa-4f2b-bf6d-86de71ef3c57" />


### 6. 특징


<img width="424" height="463" alt="image" src="https://github.com/user-attachments/assets/80fc21ca-dfc6-408b-a344-1a924fa134d8" />


**리버스 프록시 및 HTTPS 설정**


탄력적 IP 설정으로 인스턴스 재시작 시 IP 바뀌는 문제 해결


nginx로 리버스 프록시 설정, Node.js 서버의 3000번 포트를 외부에서 80번 포트로 접속 가능케 설정


certbot로 SSL(Secure Socket Layer) 인증서 발급, 외부 사이트 통해 도메인 설정 이를 통해 해당 도메인, HTTPS로만 접근 가능함


**EC2 확인**

<img width="453" height="353" alt="image" src="https://github.com/user-attachments/assets/1434be0e-4ed4-449a-bd96-1ce98fe61afa" />

**협업 관리 방안**


IAM 계정 각 조원 별 배당하여 조원들이 인스턴스 관리, 스냅샷 기능 이용 사이트 코드 변경 전 백업


<img width="693" height="227" alt="image" src="https://github.com/user-attachments/assets/89f12e13-7832-4a04-9dfc-0637690bbdcf" />


### 7. 블로그 구현 내용

<img width="679" height="431" alt="image" src="https://github.com/user-attachments/assets/f66412f0-31fe-4bba-92db-7035f1351dbf" />


<img width="825" height="430" alt="image" src="https://github.com/user-attachments/assets/9dfc6d78-185a-45c6-b31b-c7187353f4d5" />

<img width="586" height="460" alt="image" src="https://github.com/user-attachments/assets/506bed2c-c5fa-42e3-9088-644268293493" />


<img width="802" height="418" alt="image" src="https://github.com/user-attachments/assets/081cdf0b-c0e4-481c-961d-2123d46bd8a9" />


<img width="547" height="450" alt="image" src="https://github.com/user-attachments/assets/2492538a-5e40-4916-9140-2cf008e45e16" />


<img width="654" height="447" alt="image" src="https://github.com/user-attachments/assets/abcb5bc0-c1c6-421e-bd98-54af1d7d2c83" />


<img width="690" height="440" alt="image" src="https://github.com/user-attachments/assets/adcb6ea7-5de9-45e8-8432-eb3ad2f0d809" />


