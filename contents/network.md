# 네트워크



### OSI 7 Layer에 대해서 설명하세요. 

```

```

<br />
<br />


### HTTP 메소드에 대해서 설명하세요.

[ CRUD 관점에서 설명해야함 ]
Create(생성), Read(읽기), Update(갱신), Delete(삭제)

- __POST :__ 서버나 특정 리소스에 엔티티를 제출할 때 사용합니다. Create나 Update, Delete등을 할 때 사용하기도 합니다. [Create]
- __GET__ : 특정 리소스의 참조를 요청합니다. CRUD를 예로 들 경우 R에 해당합니다. url에 어느 리소스를 참조 요청하는지 드러나게 됩니다.[Read]
- __PUT__: PUT를 통해 해당 리소스를 수정합니다. UPDATE를 하지만 전체 자원을 업데이트 하는데 쓰인다고 합니다. [Update]
- __DELETE__ : 삭제 할 때 사용. 어느 자원을 삭제할 지 url에 드러나게 됩니다.[Delete]
- __PATCH__: 리소스의 부분을 수정하는데 사용합니다. 의미론적으로 UPDATE와 더 가깝다고 할 수 있습니다.

HTTP Request Method
GET : 특정 리소스의 참조를 요청합니다. CRUD를 예로 들 경우 R에 해당합니다. url에 어느 리소스를 참조 요청하는지 드러나게 됩니다.
POST: 서버나 특정 리소스에 엔티티를 제출할 때 사용합니다. Create나 Update, Delete등을 할 때 사용하기도 합니다.
PUT: UPDATE를 하지만 전체 자원을 업데이트 하는데 쓰인다고 합니다.
DELETE: 삭제 할 때 사용. 어느 자원을 삭제할 지 url에 드러나게 됩니다.
PATCH: 리소스의 부분을 수정하는데 사용합니다. 의미론적으로 UPDATE와 더 가깝다고 할 수 있습니다.

### HTTP1.1 vs HTTP2.0

__HTTP(HyperText Transfer Protocol)__

WWW(World Wide Web)에서 하이퍼텍스트(hypertext) 문서를 교환하기 위하여 사용되는 통신규약이다.

__HTTP/1.1__

Connection당 하나의 요청을 처리 하도록 설계 되어 있다. 그래서 동시전송이 불가능하고 요청과 응답이 순차적으로 이루어 지게된다. 그렇다 보니 HTTP문서안에 포함된 다수의 리소스 (CSS, JS, Images)를 처리하려면 요청할 리소스 개수에 비례해서 Latency(대기 시간)는 길어지게 된다.

__HTTP/1.1 단점__
- HOL(Head Of Line) Blocking – 특정 응답의 지연
- RTT(Round Trip Time) 증가
- 무거운 Header 구조 (특히 Cookie)

__HTTP/2.0 장점__
- __Multiplexed Streams__
 	- 한 커넥션으로 동시에 여러개의 메세지를 주고 받을 있으며, 응답은 순서에 상관없이 stream으로 주고 받는다. HTTP/1.1의 Connection Keep-Alive, Pipelining의 개선이라 보면 된다.
- __Stream Prioritization__
 - 예를 들면 클라이언트가 요청한 HTML문서안에 CSS파일 1개와 Image파일 2개가 존재하고 이를 클라이언트가 각각 요청하고 난 후 Image파일보다 CSS파일의 수신이 늦어지는 경우 브라우저의 렌더링이 늦어지는 문제가 발생한다. HTTP/2의 경우 리소스간 의존관계(우선순위)를 설정하여 이런 문제를 해결하고 있다.
- __Server Push__
  - 서버는 클라이언트의 요청에 대해 요청하지도 않은 리소스를 마음대로 보내줄 수 도 있다.
  - 클라이언트가 HTML문서를 요청했고 해당 HTML에 여러개의 리소스(CSS, Image…) 가 포함되어 있는경우 HTTP/1.1에서 클라이언트는 요청한 HTML문서를 수신한 후 HTML문서를 해석하면서 필요한 리소스를 재 요청한다.
  - HTTP/2에선 Server Push를 이용하면 클라이언트가 요청하지도 않은 (HTML문서에 포함된 리소스) 리소스를 Push 해주는 방법으로 클라이언트의 요청을 최소화 해서 성능 향상을 이끌어 낸다. 
  - 이를 PUSH_PROMISE 라고 부르며 PUSH_PROMISE를 통해서 서버가 전송한 리소스에 대해선 클라이언트는 요청을 하지 않는다.

Source. [Link](https://www.popit.kr/%EB%82%98%EB%A7%8C-%EB%AA%A8%EB%A5%B4%EA%B3%A0-%EC%9E%88%EB%8D%98-http2/)

### HTTP 응답코드에 대해서 설명하세요.

```

```

<br />
<br />


### URL 에 www.example.com 을 쳤을 때 일어나는 일들을 설명하세요.


- http://owlgwang.tistory.com/1 
- https://deveric.tistory.com/97
- [velog](https://velog.io/@jay/%EC%A3%BC%EC%86%8C%EC%B0%BD%EC%97%90-velog.io%EB%A5%BC-%EC%9E%85%EB%A0%A5%ED%96%88%EC%9D%84%EB%95%8C-%EB%AC%B4%EC%8A%A8-%EC%9D%BC%EC%9D%B4-%EC%9D%BC%EC%96%B4%EB%82%A0%EA%B9%8C-1-%EB%84%A4%ED%8A%B8%EC%9B%8C%ED%81%AC)
- https://devjin-blog.com/what-happen-browser-search/

### 사용자가 웹브라우저를 통해 서버에 이미지를 요청해서 사용자에게 보여주기까지 과정을 설명하세요

- 참고 [Link](https://krksap.tistory.com/1148?category=755546)


### HTTP와 HTTPS의 차이를 설명하세요.

- 참고: [Link]( https://post.naver.com/viewer/postView.nhn?volumeNo=16561296&memberNo=1834)


### HTTP2의 특징을 설명하세요.

```

```

<br />
<br />


### 쿠키와 세션은 언제 사용하나요?

```

```

<br />
<br />

### 파생문제
- 쿠키와 세션의 차이
- 세션은 서버에 저장되고, 쿠키는 클라이언트에 저장된다고 하셨는데, 그럼 쿠키가 안되는 상황에서도 세션은 사용할 수 있나요?

--------------------

### HTTP 프로토콜의 특징

- 비연결 지향(Connectionless) : 클라이언트가 request를 서버에 보내고, 서버가 클라이언트에 요청에 맞는 response를 보내면 바로 연결을 끊는다.
- 상태정보 유지 안 함(Stateless) : 연결을 끊는 순간 클라이언트와 서버의 통신은 끝나며 상태 정보를 유지하지 않는다.

### 쿠키와 세션의 필요성

- 참고 : https://github.com/WeareSoft/tech-interview/blob/master/contents/network.md


### DNS에 대해서 설명하세요. 

```

```

<br />
<br />


### Web으로 Server Push를 구현할 때 제약사항 등을 설명하세요.

```

```

<br />
<br />

### 3 way hand shake에 대해서 설명하세요.

```

```

<br />
<br />


### 4 way hand shake에 대해서 설명하세요.

```

```

<br />
<br />

### 흐름제어, 혼잡제어방식에 대해서 설명하세요.

```

```

<br />
<br />

------

## Challenge

### 웹 사이트를 제작했는데 고해상도 이미지를 많이 사용하여 페이지 로딩 속도가 느립니다. 최적화 하는 방법에 대해서 모두 설명하세요.

```

```

<br />
<br />


### 브라운이 새로운 검색 엔진을 개발하려고 합니다. 어떻게 설계 및 개발 것인지 아는 지식을 모두 동원하여 설명하세요.

```

```

<br />
<br />