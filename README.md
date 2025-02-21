### 💼 **Side Projects**
#### Sprout Education Web(7명)
- **기간**: 2024.09 - 2024.11
- **기술 스택**: Spring Boot, Kotlin, JPA, QueryDSL, Elastic BeanStalk, AWS EC2, RDS, CloudWatch
- **주요 기능 && 맡은 역할**:
  - **AWS 인프라 통합 및 자동화**:
    - **AWS Elastic Beanstalk**를 기반으로 RDS(MySQL), EC2, S3, CloudWatch를 통합하여 **자동화된 CI/CD 파이프라인**을 구축.
    - GitHub Actions 및 AWS CodePipeline을 사용해 코드 변경 시 자동으로 테스트와 배포가 이루어지도록 구성.
  - [NGINX 프록시 서버 커스터마이징](https://velog.io/@son93/Cors%EC%99%80-Preflightfeat.Nginx%EC%97%90-%EA%B4%80%ED%95%98%EC%97%AC):
    - **NGINX 설정 파일을 커스터마이징**하여 보안 헤더를 추가하고, Cors(option) 문제 및 Custom Header 전송 문제를 전송 문제를 해결하여 **보안 규정을 준수**.
    - CloudWatch Logs와 대시보드를 활용하여 **NGINX 로그 및 애플리케이션 메트릭을 실시간 모니터링**.
  - [데이터베이스 성능 최적화](https://velog.io/@son93/%EB%8B%A8%EC%9D%BC-%EC%9D%B8%EB%8D%B1%EC%8A%A4-vs-%EB%B3%B5%ED%95%A9-%EC%9D%B8%EB%8D%B1%EC%8A%A4-%EC%84%B1%EB%8A%A5-%EB%B9%84%EA%B5%90%EC%99%80-%EC%B5%9C%EC%A0%81%ED%99%94-%EC%82%AC%EB%A1%80):
    - 10만건의 더미데이터를 기준으로 초기 단일 인덱스 설계로 인해 발생하던 쿼리 실행 시간 **1.5~2초** 문제를, **복합 인덱스 적용 및 쿼리 최적화**를 통해 **50~150ms로 단축**하여 약 **10~30배 성능 개선**을 달성.
  - [SSE 기반 실시간 데이터 전송](https://velog.io/@son93/WebSocket-vs-SSE-%EC%96%B8%EC%A0%9C-%EC%96%B4%EB%96%BB%EA%B2%8C-%EC%82%AC%EC%9A%A9%ED%95%B4%EC%95%BC-%ED%95%A0%EA%B9%8C-feat.-Spring-Webflux):
    - 실시간 알림 처리 구현 시 **WebSocket과 SSE**를 비교하여 양방향 통신의 필요성이 없음을 판단하고 SSE(Server-Sent Events)를 채택.
    - 브라우저 종료 시에도 커넥션이 유지되는 문제를 발견하고, **30초 주기 헬스체크 쓰레드**를 구현하여 **비활성 커넥션을 자동으로 차단**하는 로직 개발.
  - **JWT 기반 인증 최적화**:
    - JWT AccessToken의 페이로드에 사용자 ID와 필수 회원 여부(`isEssential`) 정보를 포함하여, DB 호출 없이 사용자 상태를 판별.
    - 상황에 따라 HTTP 응답 코드를 즉시 반환하여, 요청당 평균 응답 시간을 30% 이상 단축하고 서버 부하를 감소.(1000건 기준  DB 조회시 200ms / Jwt 디코딩 구현시 140ms)

#### Awesome School Community App (3명)
- **기간**: 2024.04 - 2024.06
- **기술 스택**: Spring Boot, Flutter, AWS EC2, RDS, Nginx, JPA, Stomp, Oauth2, Jwt, GetX
- **주요 기능 && 맡은 역할**:
    - **백엔드 클라우드 서버 구축**: AWS EC2와 RDS를 사용하여 안정적인 백엔드 환경을 구축.
    - **리버스 프록시 설정**: Nginx를 리버스 프록시로 설정하여 클라이언트 요청을 Spring Boot 서버로 리다이렉트.
    - **JPA 활용**: 데이터베이스 테이블 설계 및 쿼리 최적화, N+1 문제 해결.
    - **실시간 채팅 기능**: WebSocket 기반 Stomp 프로토콜과 Simple Broker를 활용한 실시간 채팅 기능 구현.
    - **로그인 관리**: Oauth2와 Jwt 토큰 기반의 로그인 시스템 구현, Access token과 Refresh token 활용.
    - **상태 관리**: GetX를 사용한 Flutter 상태값 관리 및 UI 양방향 바인딩 구현.
- **링크**: 
  - [개요 및 문제해결](https://www.notion.so/2ea3e9b350f54686abddce1c4a282def)
  - [시연 영상](https://www.youtube.com/watch?v=NuTWiTgqucM)
  - [GitHub 프론트 링크](https://github.com/Higangssh/asome-fe-flutter)
  - [GitHub 백엔드 링크](https://github.com/Higangssh/Awesome_Baek)

#### Dotori Messenger Web Project (6명)
- **기간**: 2024.02 - 2024.03
- **기술 스택**: Spring Boot, React, Mybatis, WebSocket, WebRtc
- **주요 기능 && 맡은 역할**:
    - **데이터 처리**: Mybatis를 활용한 다양한 SQL 쿼리 작성 및 데이터 관리.
    - **실시간 접속 관리**: WebSocket을 활용한 실시간 접속 및 미접속 상태 관리, 다중 채팅 기능 구현.
    - **다중 음성 및 영상 통화**: WebRtc를 활용하여 P2P 연결을 위한 SDP 교환 및 ICE 협상을 중개하는 시그널링 서버 구축.
    - **API 구축**: 테이블 설계 및 RESTful API 형식에 맞춘 CRUD 기능 구현.
- **링크**: 
  - [개요 및 문제해결](https://robust-shoulder-1c6.notion.site/dotori-b47604655bd74e388a0b33d72f1e6677)
  - [시연 영상](https://www.youtube.com/watch?v=jVMS_riHU-0&t=2s)
  - [GitHub 백엔드 링크](https://github.com/Higangssh/acorn-final-be)

