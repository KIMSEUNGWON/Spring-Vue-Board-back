# Spring + Vue 게시판
게시판과 댓글을 작성할 수 있는 게시판 개발 프로젝트

## 개발 환경
+ IntelliJ
+ Postman
+ GitHub
+ H2 Database

## 사용 기술
### 백엔드
#### 주요 프레임워크 / 라이브러리
+ Java 11
+ SpringBoot
+ SpringBoot Security + JWT
+ Spring Data JPA
+ QueryDSL

#### Build Tool
+ Gradle

#### 기타 라이브러리
+ Lombok

## 핵심 키워드
+ 스프링 부트, 스프링 시큐리티, JWT를 사용하여 웹 애플리케이션 기획
+ JPA, Hibernate를 사용한 도메인 설계
+ MVC 프레임워크 기반 백엔드 서버 구축

## 프로젝트 목적
### 게시판 프로젝트를 기획한 이유?
+ 개인 프로젝트로서 쉽게 접근할 수 있으며 확장 가능성이 높습니다
+ 간단한 기능과 디자인 패턴, 새로운 라이브러리 적용이 쉽습니다
+ 기술을 학습하면서 프로젝트의 크기를 키울 수 있는 장점이 있습니다

## 핵심 기능
### SpringSecurity + JWT를 이용한 로그인 기능
로그인 기능을 위해 SpringSecurity와 토큰을 생성해주는 JWT를 사용해서 사용자에게 권한을 부여했습니다

### 게시물 기능
생성된 게시판 목록에 게시물을 작성할 수 있는 기능입니다.
기본적인 CRUD를 사용할 수 있으며 MarkDown을 사용한 것이 특징입니다
게시물의 주인만 수정과 삭제를 할 수 있는 권한이 있습니다.

### 댓글 기능
작성된 게시글에 댓글과 그 댓글에 대댓글을 작성할 수 있는 기능입니다.
댓글과 대댓글은 부모 자식 관계로 연관관계를 설정했습니다.
부모 댓글이 삭제되면 대댓글도 함께 삭제되는 구조입니다
댓글 작성자와 게시글 주인만 댓글을 확인할 수 있는 비밀 댓글 기능과 댓글 삭제 기능이 존재합니다.
댓글 작성자만 댓글을 수정할 수 있습니다.
댓글에 좋아요를 누를 수 있는 기능이 있습니다.

### 알림 기능
사용자는 자신이 작성한 게시글이나 댓글에 댓글이 달린 경우나 자신의 댓글에 좋아요를 받은 경우 알림을 받게 됩니다.
알림을 읽으면 해당 댓글이 생성된 페이지로 이동하게 됩니다

### 외부 API 적용
Pokemon API라는 외부 API를 사용해서 Pokemon에 대한 정보를 제공하는 게시글 기능입니다.

### WebSocket을 활용한 간단한 채팅 기능
STOMP를 사용해서 유저들끼리 채팅을 할 수 있는 기능입니다.