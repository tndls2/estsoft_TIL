📍 [Internet](#internet)  
📍 [HTTP & HTTPS](#http--https)  
📍 [IP](#ip)  
📍 [PORT](#port)  
📍 [DNS](#dns)


# 🎆 네트워크 기초
## Internet
- 전 세계적으로 연결되어있는 `컴퓨터 네트워크 통신망`
- 글로벌하게 연결된 컴퓨터 네트워크의 시스템
- 웹(World Wide Web), 전자메일, 파일공유(Torrent), 동영상 스트리밍, 온라인게임, 모바일앱 등 다양한 서비스들을 포함
- `프로토콜(TCP/IP)`을 기반으로 통신

   ![internet](https://www.books.weniv.co.kr/images/basecamp-html-css/chapter01/01-1.png)
   > 🚨 Web !== Internet  
   >    웹은 인터넷과 다르며, 웹은 인터넷을 기반으로 한 수많은 서비스 중 하나  
   >    `인터넷` = 인프라(기반 구조)  
   >    `웹` = 그 위에서 동작하는 서비스 중 하나
   >    ![web vs internet](https://www.books.weniv.co.kr/images/basecamp-html-css/chapter01/01-2.png)


## HTTP & HTTPS
웹 서버와 클라이언트(보통 웹 브라우저) 간의 데이터를 주고받는 방식을 정의하는 프로토콜

   > 💡 프로토콜   
   >  전송 규칙, 약속  
   >  컴퓨터나 장치 간에 데이터를 주고받는 전송 규칙 또는 약속  
   >  웹 위에 있는 다양한 서비스들(인터넷, FTP, SSH, 이메일 등)은 각기 다른 프로토콜 사용
   > | 이름 | 프로토콜 |  
   > | --- | --- |  
   > | WWW(웹) | HTTP/HTTPS |  
   > | FTP(파일전송) | FTP/SFTP |  
   > | Email(이메일) | SMTP/POP3/IMAP|  


### ✅ HTTP (HyperText Transfer Protocol)

```
http://www.google.com:80/app/index.html
```

클라이언트와 서버 간의 hypertext 문서(주로 HTML)를 주고받기 위한 프로토콜

<특징>
- `비연결성(Connectionless)`: 각 요청은 독립적으로 처리되며, 한 요청이 완료된 후에는 연결이 끊김
- `무상태성(Stateless)`: 서버는 각 요청을 독립적으로 처리하며, 이전 요청의 상태 기억 ❌

<br>

### ✅ HTTPS (HyperText Transfer Protocol Secure)

```
https://www.google.com:443
```

HTTP의 보안 버전 ➡️ 클라이언트와 서버 간의 데이터 암호화

<특징>
- `보안성`: `SSL/TLS`를 통해 데이터 암호화

## IP
Internet Protocol의 약자

통신 단위: Packet (Package + Bucket)

**✅ 클라이언트의 패킷 전달**

![클라이언트 패킷 전달](https://miro.medium.com/v2/resize:fit:1100/format:webp/1*Y9VXeNZStE-Q8ZpNEUrLZQ.png) 

**✅ 서버의의 패킷 전달**

![서버 패킷 전달](https://miro.medium.com/v2/resize:fit:1100/format:webp/1*t1AVYP8-LR4_7U68cGn-pg.png)   

**🚨 문제점**

1. `비연결성` : 도착지 서버가 서비스 불능 상태일 경우
   
    ![비연결성](https://miro.medium.com/v2/resize:fit:1100/format:webp/1*tBY4Mjdm-jgqjdUEZiKY9A.png)   

   서버가 패킷을 받을 수 있는 상태가 아니지만, 출발 시점에 이를 알 수 없음

3. `비신뢰성`
   
    (1) 패킷 소실
   <br>
   
   ![비신뢰성](https://miro.medium.com/v2/resize:fit:1100/format:webp/1*U7bUIrhCbnO4vGiIHaNfag.png)   
    <br>
    (2) 패킷 전달 순서 보장 ❌
   <br>
   
   ![비신뢰성2](https://miro.medium.com/v2/resize:fit:1100/format:webp/1*_q9Et3jBxpekTETs_3iqkg.png)   
   <br>

**💡 해결**  : `TCP 프로토콜`

## PORT
컴퓨터가 각종 신호를 받아들이고 내보낼 수 있도록 연결하는 연결 단자

같은 IP 내에서 프로세스를 구분 ➡️  하나의 IP 안에서 여러 요청을 접속 가능

✅ `0 ~ 65535`까지 할당 가능 but `0 ~ 1023`까지는 이미 누군가 사용하고 있는 포트라 사용하지 않는 것이 좋음
- 대표적인 0 ~ 1023 사용 포트
    - HTTP : 80 포트
    - HTTPS : 443 포트
    - TELNET : 23 포트
    - FTP : 20, 21 포트
    - SSH : 22 포트

![port](https://velog.velcdn.com/images/whwogur/post/77a1b90f-219b-431b-a831-7040b24c7b13/image.png) 
ex) 게임: 8090, 화상통화: 21000, 웹 브라우저: 10010번 포트로 접속 가능

## DNS
Domain Name System의 약자

인터넷을 편리하게 사용할 수 있도록 제공해주는 체계

✅ DNS 서버 : 도메인 주소 ➡️ IP로 반환해주는 역할

![title](https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2Fd1Mue8%2FbtqM0rYpQ5E%2FD5GKh2Qv8Sqm2RAkwc6Tb1%2Fimg.jpg)   
