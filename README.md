## 개요
금번 활동을 통해 Private Cloud 환경을 구축하는 방법에 대해 이해한다.




## 목표 아키텍처

해당 메뉴얼을 통해 Kubernetes 기반의 Private Cloud 시스템 구축을 수행한다. (TA,PA 영역)

또한 보안상 이슈가 될 수 있는 Service Migration 관련된 내용은 포함하지 않는다. 


![1](https://user-images.githubusercontent.com/53555895/82279300-2b2afa80-99c7-11ea-829a-7893e925812e.PNG)


## 수행 절차

K8S기반 Private Cloud System 실행/운영 환경을 구성하며, 다음 절차에 따라 진행한다.

   1. Infra 구성(VM구축)
   2. Kubernetes(Master/Node) 구성
   3. Internal Network 구성
   4. Private Registry 구성
   5. Application Load Balancer 구성
   5. Shared Storage(NFS) 구성
   6. CI/CD 구성
   7. Monitoring(Prometheus/Grafana) 구성
   8. Logging(ELK) 구성
   9. Application Mig. (Refactoring)
   10. Cloud Native. (Rebuild)



## Infra 구성(VM구축)

### 1. 인프라 아키텍처

![3](https://user-images.githubusercontent.com/53555895/82279296-29f9cd80-99c7-11ea-91f0-c83ec1acc703.jpg)


### 구성 VM 내역

다음 스펙으로 VM주문한다. (물론 테스트 환경이므로 최저 구성한 스펙이며, 실제 운영 환경은 훨씬 고스펙이 필요하다.)

|*용도*|*Hostname*|*CPU*|*MEM*|*Disk*|
|-|-|-|-|
|Master|test-master|2Core|2GB|50GB|
|Node1|test-node1|2Core|4GB|50GB|
|Node2|test-node2|2Core|4GB|50GB|
|Node3|test-node3|2Core|4GB|50GB|



### CentOS 이미지 다운로드

아래 다운로드 링크에서 이미지를 다운로드 한다.
일반적으로 RedHat계열(RedHat, CentOS등)과 Ubuntu계열을 많이 쓰나, 금번 테스트는 RedHat계열인 CentOS를 사용한다.

CentOS이미지에도 DVD ISO / Everything ISO / Minimal ISO 등 여러가지가 존재하나,
일반적으로 On-premise에서는 DVD ISO를 주로 사용하며, Public Cloud에서는 Minimal을 주로 사용한다. (사유 X-Windows 유무)


```
http://ftp.kaist.ac.kr/CentOS/7.8.2003/isos/x86_64/
```




## 목표 아키텍처

### 2. 서비스 아키텍처
![2](https://user-images.githubusercontent.com/53555895/82279301-2bc39100-99c7-11ea-9ebb-55ff9b6bb3e0.PNG)







## K8S기본 구성

