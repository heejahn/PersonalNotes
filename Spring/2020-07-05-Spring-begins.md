---
title: "스프링 환경 설정"
excerpt: "Chapter 1. 스프링 시작"
comments: true

categories:
  - Spring
last_modified_at: 2020-07-05
---
#### 해당 카테고리는...
최범균 저자가 쓴 "초보 웹 개발자를 위한 스프링 프로그래밍 입문 5" 내용이다.  
책을 읽으며 기록하고, 이해한 걸 정리하기 위해 시작했다.

### 스프링 프레임워크
##### 특징
* 의존 주입 (Dependency Injection)
* AOP (Aspect-Oriented Programming)
* MVC 웹 프레임워크
* JDBC, JPA 연동, 선언적 트랜잭션 처리, DB 연동

스프링 프레임워크는 여러 스프링 관련 프로젝트를 함께 사용한다.   
스프링 데이터 : 적은 양의 코드로 데이터 연동 처리를 도와줌. JPA, 몽고DB, 레디스 등 저장소 기술을 지원   
스프링 시큐리티 : 웹 접근 제어, 객체 접근 제어, 오픈 ID, LDAP 등 다양한 인증 방식과 암호화 기능 제공   
그 외 : 스프링 인티그레이션, 스프링 하둡, 스프링 소셜 등.   
프로젝트 설명 : <https://spring.io>

이 서적은 기초만 다루기에 AOP의 Before Advice/After Advice나, JPA/MyBatis 연동, 시큐리티 등은 따로 공부해야 한다.   
우선 기본기를 다지고 나중에 배워봐야 겠다.

#### 설치
Java와 이클립스는 이미 설치 되어 있기에 스킵한다.   
메이븐을 다운 받아야 한다.   
왜냐면 스프링 프레임워크를 사용하기 위한 모듈 중 스프링에 포함되지 않은 모듈(aopalliance, spring-orm)은 메이븐 중앙 리포지토리를 통해 받을 수 있다.

##### 메이븐(Maven) 설치
이클립스를 이용하면 직접 설치가 필요없지만, 후에 할 웹 어플리케이션 파트 때 톰캣 없이 실행시키기 위해 설치함.   
아파치 사이트에서 최신 버전을 다운로드 하면 된다.   
메이븐 설치 사이트 : <http://maven.apache.org/>   
다운로드 페이지에 들어가면 다운 받는 옵션이 4개 있는데, 직접 메이븐을 만들 생각이 아니면 이미 구성된 binary를 받으라 한다.   
tar.gz와 zip 옵션이 있는데, 나는 윈도우 유저라 zip파일을 선택했다.

저자는 찾기 쉽게 C 드라이브 밑에 devtool 폴더를 새로 생성해 파일을 넣으라 추천해줘 그대로 실행했다.   
압축을 풀고 bin 폴더 내에 mvn 파일이 있으면 된다.   
그 다음 환경변수로 가서 사용자 변수 내 Path에서 bin 폴더 주소를 추가해서 맨 위로 올려주면 된다.   

메이븐이 잘 실행 되는지 cmd에서 확인한다.
```
mvn -version
```
아무 에러 메시지 없이 메이븐에 대한 정보가 나온다면 설치 성공이다.

##### 그레이들(Gradle) 설치
그레이들도 메이븐과 똑같은 절차를 밟으면 된다.   
그레이들 설치 사이트 : <https://gradle.org/releases/>   
참고로 사이트에서 혼자 따라할 수 있는 튜토리얼과 매달 실시간 온라인 수업을 연다.   
튜토리얼 : <https://gradle.org/guides/>   
온라인 수업 : <https://gradle.com/training/>   
그레이들은 따로 공부하라 하니, 해볼까 한다.   
다만, 실시간 온라인 수업은 미국 시간 기준으로 아침에 열어서 패쓰하기로 했다.   

```
gradle -version
```
똑같이 잘 나온다.   
이제 Spring을 배울 준비는 완료다.