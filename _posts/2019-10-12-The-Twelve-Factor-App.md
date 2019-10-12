---
title: "The Twelve Factor App"
date: 2019-10-12 21:38:28 -0400
categories: jekyll update
---

마이크로 아키텍쳐 공부를 하는 도중에 소프트웨어 서비스에 대해 정의한 사이트에 대해 알게되었다.

[12-factor-app]: https://12factor.net/ko/codebase
최근 소프트웨어를 서비스 형태로 제공하는게 일반화 되면서, 웹앱 혹은 SaaS(Software As A Service)라고 부르게 되었다.Twelve-Factor app은 아래 특징을 가진 SaaS 앱을 만들기 위한 방법론이다.

* 설정 자동화를 위한 절차(declarative) 를 체계화 하여 새로운 개발자가 프로젝트에 참여하는데 드는 시간과 비용을 최소화한다.
* OS에 따라 달라지는 부분을 명확히하고, 실행 환경 사이의 이식성을 극대화 한다.
* 최근 등장한 클라우드 플랫폼 배포에 적합하고, 서버와 시스템의 관리가 필요없게 된다.
* 개발 환경과 운영 환경의 차이를 최소화하고 민첩성을 극대화하기 위해 지속적인 배포가 가능하다.
* 툴, 아키텍처, 개발 방식을 크게 바꾸지 않고 확장(scale up) 할 수 있다.


Twelve-Factor 방법론은 어떤 프로그래밍 언어로 작성된 앱에도 적용할 수 있고 백엔드 서비스(데이터베이스, 큐, 메모리 캐시 등)와 다양한 조합으로 사용할 수 있다.


## I. Codebase

Twelve-Factor앱은 항상 깃과 같은 버전 컨트롤 시스템을 사용하여 변화를 추적하며, 이를 code repository 라고 부른다.
Codebase는 단일저장소일수도 있고 커밋을 공유하는 여러가지 저장소 일수도 있다.
코드베이스는 app사이에 1:1관계가 유지되어야한다. 코드베이스가 여러개일 경우 이는 분산시스템이 되어버림.
(하둡같은 경우 slave노드가 다 같은 역할을 하지만 이경우는 각기 다른 역할을 해야한다.)
또한 개별앱은 Twelve-Factor를 따른다.


![Alt text](/img/codebase-deploys.png)


여러앱이 동일한 코드를 공유할시 Twelve-Factor를 위반하는것이며 즉시 공유코드를 라이브러리화 시키며,
이를 종속성 매니저(dependency manager) 로 관리해야한다.


## II. Dependencies
