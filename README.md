# 42 Seoul Project
## <ft_irc> (참여: taehykim, mikim3, jokang)

 <br>
IRC 프로토콜 사용 <br>
IRC 참고자료 : https://datatracker.ietf.org/doc/rfc2812/ <br>
비동기식 논블로킹 멀티플렉서 TCP 통신 채팅프로그램 서버부 개발<br>
Client, Server, Channel을 각각 객체로써 관리. <br>
Language : C++ <br>
poll함수 이용 <br>
<br>

### <사용 방법>
```c
// Server

make
./ircserv <port> <password>
```

```c
// Client

// 1. irssi 이용 접속
brew install irssi

irssi
/connect <address> <port> <password> <username>
/join #<channel>	// 채널 개설 및 입장
/part #<channel>	// 채널 나가기
/quit				// 연결 끊기
/exit				// irssi 종료
/mode #<channel> +o <nickname>	// operator 이관
/mode #<channal> +k <password>	// 채널 비밀번호 설정
/mode #<channel> +l <number>	// 채널 인원수 제한
/kick #<channel> <nickname>		// 채널에서 강퇴
/notice #<channel> :<msg>		// 공지올리기

/nick <nickname>		// nickname 변경
```

```c
// Client

// 2. nc 이용 접속

nc <address> <port>
PASS <password>		// password 설정
NICK <nickname>		// nickname 설정
USER <user> <mode> <unused> <realname>	// user 정보입력

JOIN #<channel>	// 채널 개설 및 입장
PART #<channel>	// 채널 나가기
QUIT			// 연결 끊기
MODE #<channel> +o <nickname>	// operator 이관
MODE #<channal> +k <password>	// 채널 비밀번호 설정
MODE #<channel> +l <number>		// 채널 인원수 제한
KICK #<channel> <nickname>		// 채널에서 강퇴
NOTICE #<channel> :<message>	// 공지올리기
PRIVMSG <user> :<message>		// 채널에 채팅글 쓰기

NICK <nickname>		// nickname 변경
```
