# 🖥️  On-Premise 3-tier Architecture Project

Cloud Bootcamp 기간 동안 우리 팀에서 수행한 On-Premise 3 Tier Architecture 프로젝트

![image](https://user-images.githubusercontent.com/76054852/230912393-54f73945-a501-4db3-8281-8e6c88b4eb47.png)

> 기술 문서 및 프리젠테이션 pdf 파일이 포함되어 있습니다.

🌐 [PROmet](https://github.com/Waji-97/PROmet-Website) - Django 프레임워크를 사용하여 만든 PROmet 웹사이트

☁️ [AWS Cloud](https://github.com/Waji-97/PROmet-Cloud-Migration-Project) - AWS 클라우드 버전


## 💡 목표

이 온프레미스 3계층 인프라의 목표는 PROmet 구직 웹사이트를 온프레미스 인프라에 배포하는 것이었습니다. PROmet은 구직자가 이력서, 포트폴리오, 자기소개서를 등록할 수 있는 플랫폼을 제공합니다. 그런 다음 파트너 회사는 필요에 맞는 잠재적 후보자를 스카우트하여 구직자와 고용주 모두에게 더 나은 기회를 제공할 수 있습니다.

## ⛏️ 목표 및 설계
프로젝트는 여러 부분으로 나뉩니다. 먼저 구직자가 이력서, 포트폴리오, 자기소개서를 등록할 수 있도록 Django 기반 시스템을 구현했습니다. 우리는 이를 달성하기 위해 Apache, HAProxy, GlusterFS, MariaDB 및 OpenSSL을 포함한 여러 기술을 사용했습니다. 그런 다음 WEB/WAS 서버를 배치하고 GlusterFS 서버를 생성하여 연결하고 Proxy, DNS, DB 서버를 연결하여 그림과 같이 On-Premise 인프라를 구축했습니다. 프로젝트에서 나의 역할은 제안 및 계획, Django 앱 생성, WAS 서버 배포, GlusterFS 서버 생성 및 연결, 프록시, DNS 및 DB 서버 통합을 포함했습니다. 각각의 서버와 솔루션을 설계하고 연결하여 안정적인 인프라를 구축했습니다. 마지막으로 각 서버를 모니터링하고 관리하기 위한 셸 스크립트를 작성했습니다.

## 📝 결론

이 프로젝트를 통해 다양한 기술과 솔루션을 사용하여 온프레미스 3계층 인프라를 구축하는 방법을 배웠습니다. 또한 각 서버를 연결할 때 발생하는 문제를 해결하는 방법도 배웠습니다. 프로젝트를 진행하는 동안 많은 어려움이 있었지만 한 가지 중요한 문제는 슬레이브 DB 서버를 읽기 전용 복제본으로 복제하도록 구성하는 것이었습니다. Django 프로젝트에 Python 파일을 추가하여 읽기 전용 트래픽을 Slave DB로, 기타 작업을 Master DB로 라우팅하여 이 문제를 해결했습니다. 이를 통해 Master DB의 부하를 크게 줄이고 읽기 작업의 부하를 Replication Slave DB로 분산시켰습니다. 이 기술적 문제 해결 프로세스를 통해 새로운 기술과 솔루션을 습득하여 더 나은 역량을 개발할 수 있었습니다.
