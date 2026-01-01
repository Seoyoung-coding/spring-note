# 학습 목표
Spring Boot의 등장 배경과 장점을 설명할 수 있다
Spring Initializr를 사용하여 Spring Boot 프로젝트를 생성할 수 있다
build.gradle 파일의 구성 요소와 의존성 관리 방법을 이해할 수 있다
@SpringBootApplication 어노테이션의 역할을 설명할 수 있다
IoC 컨테이너와 DI의 개념을 이해하고 활용할 수 있다
Bean의 생명주기와 스코프를 이해하고 관리할 수 있다
컴포넌트 스캔과 자동 주입을 활용할 수 있다
Profile을 사용한 환경별 설정을 구성할 수 있다


## REST API
- 웹에서 데이터를 주고받는 효율적이고 표준화된 방법으로, 애플리케이션 간 연동을 쉽게 만들어주는 핵심적인 기술
- IoC(Inversion of Control) = 
- DI(Dependency Injection) = 

### 자원(Resource): 모든 것을 명사(URL)로 표현됨 (예를 들어 사용자 정보는 /users)
HTTP 메서드(Verb): 행위(Verb)
- GET: 데이터 조회 (Read).
- POST: 데이터 생성 (Create).
- PUT: 데이터 수정 (Update).
- DELETE: 데이터 삭제 (Delete).

### 과정
URL로 자원을 식별하고 GET, POST, PUT, DELETE 같은 HTTP 메서드(동사)를 사용해 데이터 조회, 생성, 수정, 삭제(CRUD) 등의 작업을 수행함
- 1) 클라이언트가 특정 자원(URL)에 대해 HTTP 메서드(GET, POST 등)를 사용해 요청을 보낸다
- 2) 서버는 요청을 받아 해당 자원에 대한 작업을 수행함 (CRUD).
-3) HTTP 상태 코드(200 OK, 404 Not Found 등)와 함께 데이터(JSON 등)로 응답

### 장점
- 유연성 및 확장성: 상태 비저장 방식으로 인해 서버 부하가 적고 확장이 용이함
- 보편성: HTTP 표준을 기반으로 하므로 다양한 플랫폼과 언어에서 쉽게 사용할 수 있다
- 가독성: 명확한 자원(URL)과 행위(메서드)를 통해 요청의 의도를 파악하기 쉽다

## 컨트롤러 설정하기
- 1) @RestController = @Controller + @ResponseBody
수많은 클래스 중에서 직접 객체로 만들어(Bean) loC 컨테이너에 넣어두고 관리하라고 신호를 주는 것. URL 주소와 메서드를 연결(Mapping)할 수 있게 됨
- 2) @GetMapping = 브라우저에서 특정 주소로 접속(GET 요청)했을 때, 아래에 있는 메서드를 실행하라는 의미
