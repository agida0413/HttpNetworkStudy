# URI



> [!NOTE]
>
> - **URI 단어 뜻**
>
>   -  Uniform: 리소스 식별하는 통일된 방식 
>   -  Resource: 자원, URI로 식별할 수 있는 모든 것(제한 없음) 
>   -  Identifier: 다른 항목과 구분하는데 필요한 정보 
>
>   
>
>   -  URL: Uniform Resource Locator
>   -  URN: Uniform Resource Name
>
> 





# 모든 것이 HTTP

> [!NOTE]
>
> - HTML, TEXT • IMAGE, 음성, 영상, 파일
> - JSON, XML (API) 
> - 거의 모든 형태의 데이터 전송 가능 
> - 서버간에 데이터를 주고 받을 때도 대부분 HTTP 사용



# HTTP 특징

> [!NOTE]
>
> - **클라이언트 서버구조**
>
>   - Request Response 구조 
>   - 클라이언트는 서버에 요청을 보내고, 응답을 대기 
>   -  서버가 요청에 대한 결과를 만들어서 응답
>
>   
>
> - **무상태 프로토콜**
>
>   - 서버가 클라이언트의 상태를 보존X 
>   -  장점: 서버 확장성 높음(스케일 아웃) 
>   -  단점: 클라이언트가 추가 데이터 전송
>
> - HTTP 메시지
>
> - **단순함, 확장가능**



# Stateful,Stateless

> [!NOTE]
>
> - **상태 유지**: 중간에 다른 점원으로 바뀌면 안된다. (중간에 다른 점원으로 바뀔 때 상태 정보를 다른 점원에게 미리 알려줘야 한다.) 
>
> -  **무상태**: 중간에 다른 점원으로 바뀌어도 된다. 
>
>   -  갑자기 고객이 증가해도 점원을 대거 투입할 수 있다. 
>   -  갑자기 클라이언트 요청이 증가해도 서버를 대거 투입할 수 있다.
>
> -  무상태는 응답 서버를 쉽게 바꿀 수 있다. -> **무한한 서버 증설 가능**
>
> - **Stateless 실무 한계** 
>
>   -  모든 것을 무상태로 설계 할 수 있는 경우도 있고 없는 경우도 있다. 
>
>   -  무상태 
>
>     -  예) 로그인이 필요 없는 단순한 서비스 소개 화면
>
>   - 상태 유지
>
>     - 예) 로그인 
>
>   -  로그인한 사용자의 경우 로그인 했다는 상태를 서버에 유지
>
>   - 일반적으로 브라우저 쿠키와 서버 세션등을 사용해서 상태 유지 
>
>   - 상태 유지는 최소한만 사용
>
>      



# 비 연결성

> [!NOTE]
>
> - HTTP는 기본이 연결을 유지하지 않는 모델 
> -  일반적으로 초 단위의 이하의 빠른 속도로 응답 
> -  1시간 동안 수천명이 서비스를 사용해도 실제 서버에서 동시에 처리하는 요청은 수십개 이 하로 매우 작음 
>   - 예) 웹 브라우저에서 계속 연속해서 검색 버튼을 누르지는 않는다. 
> -  서버 자원을 매우 효율적으로 사용할 수 있음



# 비 연결성 한계와 극복

> [!NOTE]
>
> - TCP/IP 연결을 새로 맺어야 함 - 3 way handshake 시간 추가 
> - 웹 브라우저로 사이트를 요청하면 HTML 뿐만 아니라 자바스크립트, css, 추가 이미지 등 등 수 많은 자원이 함께 다운로드 
> -  지금은 HTTP 지속 연결(Persistent Connections)로 문제 해결 
> -  HTTP/2, HTTP/3에서 더 많은 최적화

