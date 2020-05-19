## 목표 아키텍처
### 1. 인프라 아키텍처
![1](https://user-images.githubusercontent.com/53555895/82279300-2b2afa80-99c7-11ea-829a-7893e925812e.PNG)

### 2. 서비스 아키텍처
![2](https://user-images.githubusercontent.com/53555895/82279301-2bc39100-99c7-11ea-9ebb-55ff9b6bb3e0.PNG)


## Centos 설치

### CentOS 이미지 다운로드

아래 다운로드 링크에서 이미지를 다운로드 한다.

일반적으로 RedHat계열(RedHat, CentOS등)과 Ubuntu계열을 많이 쓰나, 금번 테스트는 RedHat계열인 CentOS를 사용한다.


```
http://ftp.kaist.ac.kr/CentOS/7.8.2003/isos/x86_64/
```

DVD ISO / Everything ISO / Minimal ISO 등 여러가지가 존재한다.
일반적으로 On-premise에서는 DVD ISO를 주로 사용하며, Public Cloud에서는 Minimal을 주로 사용한다.
(사유 X-Windows 유무)






## K8S기본 구성
![3](https://user-images.githubusercontent.com/53555895/82279296-29f9cd80-99c7-11ea-91f0-c83ec1acc703.jpg)
