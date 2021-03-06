# 프로젝트 의존성
- node.js
- npm
- mongodb : DB 서버
- redis : ChatServer 관리 캐시, Session 캐시, ChatServer 클러스터링
- haproxy : 로드밸런서
- nginx : 정적파일, 이미지 캐싱 리버스 프록시
- [authServer](https://github.com/seungjoopet/AuthApiServer) : 로그인과 회원가입을 관리하는 서버
- [imageServer](https://github.com/Crazy0416/imageServer) : 이미지 업로드용 서버
- [W.A.Server](https://github.com/Crazy0416/WasServer) : 웹 어플리케이션 서버
- [chatManageServer](https://github.com/Crazy0416/ChatManageServer) : 채팅 서버 관리 및 로드밸런싱 서버
- [chatServer](https://github.com/shh0258/NettyForChatServerOfRedisCluster) : 채팅서버

# 프로젝트 시연영상
[유튜브 영상](https://www.youtube.com/watch?v=eHSZN2g1drE)

# 프로젝트 구조
![태그톡 구조](https://github.com/seungjoopet/AuthApiServer/blob/master/%EC%84%9C%EB%B9%84%EC%8A%A4%20%EA%B5%AC%EC%84%B1.png)

# 프로젝트 설치
## 소스코드 복제
```
git clone https://github.com/Crazy0416/imageServer
cd imageServer
npm install
```
## nginx 설정
- nginx는 5000번 포트에서 LISTEN.
- nginx는 리버스 프록시로 동작한다.
- nginx에서 정적파일들을 처리한다.
- POST요청으로 이미지 업로드 요청이 올 시에 imageServer로 요청을 pass 한다.