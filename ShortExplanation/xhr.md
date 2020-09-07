### xhr(XMLHttpRequest)

ajax 요청을 생성하는 JavaScript API.   
브라우저와 서버 간의 네트워크 요청을 전송할 수 있다.   
ajax를 이용하니까 새로 고침 없이 URL로부터 데이터를 받아올 수 있다.   
<br>
이름은 XML이지만 모든 형태의 데이터를 받아올 수 있고 여러 프로토콜을 지원(HTTP, FTP, File)한다.   
완전한 양방향 통신에는 웹 소켓 이용을 추천한다.    
<br>

### xhr과 websocket 차이점
xhr은 클라이언트에서 서버로 요청을 하는 단방향 통신이라면 websocket은 어느 방향으로든 요청을 보낼 수 있는 양방향 통신이다.   
websocket은 양방향 통신이라 실시간 통신이 가능해 실시간 채팅, 주식 등의 서비스에서 사용된다.    
대신 지속적으로 통신을 유지해야 하는 만큼 기능 부하가 생길 수 있고, 의도치 않게 연결이 끊어질 경우를 대비해야 한다.   