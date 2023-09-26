# 실습을 위한 개발 환경 세팅
* https://github.com/slipp/web-application-server 프로젝트를 자신의 계정으로 Fork한다. Github 우측 상단의 Fork 버튼을 클릭하면 자신의 계정으로 Fork된다.
* Fork한 프로젝트를 eclipse 또는 터미널에서 clone 한다.
* Fork한 프로젝트를 eclipse로 import한 후에 Maven 빌드 도구를 활용해 eclipse 프로젝트로 변환한다.(mvn eclipse:clean eclipse:eclipse)
* 빌드가 성공하면 반드시 refresh(fn + f5)를 실행해야 한다.

# 웹 서버 시작 및 테스트
* webserver.WebServer 는 사용자의 요청을 받아 RequestHandler에 작업을 위임하는 클래스이다.
* 사용자 요청에 대한 모든 처리는 RequestHandler 클래스의 run() 메서드가 담당한다.
* WebServer를 실행한 후 브라우저에서 http://localhost:8080으로 접속해 "Hello World" 메시지가 출력되는지 확인한다.

# 각 요구사항별 학습 내용 정리
* 구현 단계에서는 각 요구사항을 구현하는데 집중한다. 
* 구현을 완료한 후 구현 과정에서 새롭게 알게된 내용, 궁금한 내용을 기록한다.
* 각 요구사항을 구현하는 것이 중요한 것이 아니라 구현 과정을 통해 학습한 내용을 인식하는 것이 배움에 중요하다. 

### 요구사항 1 - http://localhost:8080/index.html로 접속시 응답
* 한 번 요청 - 여러 개의 추가 요청 발생
  서버가 웹 페이지를 구성하는 모든 자원을 한 번에 응답하지 않음. url요청에 대한 응답에 html만 보냄
* URI : 서버가 유일하게 식별할 수 있는 클라이언트의 요청 자원 경로


### 요구사항 2 - get 방식으로 회원가입
* 요청 - 여러 개의 추가 요청 발생. 웹 서버는 /index.html 요청에 대한 응답에 html만 보냄.
  클라이언트가 여러 리소스(html, css, image 등등)에 대한 추가적인 요청을 서버에 보냄
* 요청 헤더 <필드 이름 > : <필드 값>
* 응답 문서 구성 mehtod속성, 요청 URI : action tag ? 매개 변수 : 쿼리 스트링 
### 요구사항 3 - post 방식으로 회원가입
* REST API 설계와 AJAX 기반 웹 애플리케이션 개발 - PUT, DELETE METHOD 까지 활용하여 개발

### 요구사항 4 - redirect 방식으로 이동
* 새로고침 : 유지하던 요청을 다시 요청 - 데이터 중복 전송
* 리다이렉트 : 지정한 LOCATION 경로로 서버에 재요청 

### 요구사항 5 - cookie
* session 

### 요구사항 6 - stylesheet 적용
* CSS REQUEST : Content-Type : text/css
stringValue().endsWith("string***");
### heroku 서버에 배포 후
* 
