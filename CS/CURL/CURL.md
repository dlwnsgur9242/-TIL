# CURL

## CURL이란?
+   CURL 이란?
    -   URL 기반으로 데이터를 웹(서버)로 전송하기 위한 명령줄 유틸리티다.
    -   별도의 view나 툴없이 직접 서버에 http request을 날리고 response를 확인할 수 있다.
    -   curl 을 사용하면 HTTP, HTTPS, SCP, SFTP 및 FTP 등 다양한 프로토콜과 Proxy, Header, Cookie 등 세부 옵션까지 쉽게 설정할 수 있다.
    -   서버 API test 도구 중 postman 과 같은 역할을 할 수 있다. 

## CURL 사용법
+   CURL 사용법
    -   curl [option] [URL]
    -   가장 간단한 형태는 'curl example.com'이다
    -   프로토콜을 지정하지 않은 경우, curl은 사용할 프로토콜을 추측하려고 시도하며, 이 프로토콜은 HTTP로 기본 설정된다.
    
    -X : http method 를 get/post로 할건지 지정 지정없으면 디폴트는 get
    -H : http 헤더값
    -d : http body값 or 함께 전달할 파라미터 값
    -G : 전송할 사이트 url 및 ip 주소
    -I : 사이트의 Header 정보만 가져오기
    -i : 사이트의 Header와 바디 정보를 함께 가져오기
    -u : 사용자 정보


## CURL 사용법 

+   📍요청시 자세한 정보 표시
    -   curl -v [URL]

+   📍post 요청 보내기
    -   curl -X POST [URL]

+   📍data 같이보내기 
    -   curl -X POST —data "name=john&age=10" [URL]

+   📍form 보내기
    -   curl  -d name="John Grib"  -d hobby="coding" [URL]

+   📍 json 보내기
    -   curl -d '{"name":"john"}'  -H "Content-Type: application/json" [URL]

+   📍출력을 파일에 저장
    -   curl 명령의 결과를 저장하려면 -o 또는 -O 옵션을 사용한다.
    -   소문자 -o : 미리 정의된 파일 이름을 사용하여 파일을 저장한다.
    -   curl -o [저장할 파일 이름] https://[접근할 URL]
    -   대문자 -O : 파일을 원래 파일 이름으로 저장한다.
    -   curl -O htttps://[접근할 URL]


## CURL 실습
+ 명령어
    -   C:\Users\USER>curl -X POST -H "Content-Type: application/json" -d "{\"username\": \"test_user\", \"password\": \"123456\"}" https://jsonplaceholder.typicode.com/posts

+   출력결과
    -   {
    -    "username": "test_user",
    -    "password": "123456",
    -    "id": 101
    -    }