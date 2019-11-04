---
title: "What is Server"
date: 2019-11-04 00:00:00 -0400
categories: jekyll update
---
## 서버(Server): 다른 곳에서 받은 요청을 처리해주는 프로그램을 말한다.

http 프로토콜을 이용하여 데이터를 주고 받을 수 있는 웹서버를 만들고 그 위에
채팅서버 , 위치기반 서비스 서버, 모바일 서버, JSON-RPC 같은 기능을 추가함

* JSON-RPC:

  JSON 형식으로 표준 데이터 포맷을 정해두고 RPC(Remote Procedure Call) 방식으로 데이터를 주고 받는다.
  클라이언트에서 함수를 호출하듯이 서버에 데이터를 요청할 수 있다.


* 위치 기반 서비스 서버 :

 - 공간 인덱싱 (Spatial Indexing): R 트리를 이용해 공간 데이터를 빠르게 탐색하도록 한다.
 - 공간 데이터 저장 (Spatial Data Store): 위치 데이터 저장
 - 공간 데이터 검색(Spatial Data Search)

 ex) 위치데이터를 전송하면 저장하기도 하고 특정위치의 instance 를 모두 찾아줄 수 있다.

 * 모바일 서버 :

 - 웹서버랑 비슷하지만 모바일일 관련된 기능을 추가 (단말 관리, 푸시 서비스)
