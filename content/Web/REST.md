---
title: REST(ful)
---

### 1 . 1 . 3 REST(ful)

#### REST(Representational State Transfer)의 주요 특징
1. HTTP 프로토콜 사용
2. 상태 비저장(Stateless)
3. 캐시 가능
4. 리소스 기반

#### RESTful Web Service 의 핵심 개념
  - `Resource` : 작업을 수행할 수 있는 데이터
  - `Endpoint` : 고유한 URL 과 HTTP 동사(동작)로 구성된 기능 접근

#### HTTP 동사와 CRUD 작업의 대응
  - `POST` : 생성(Create)
  - `GET` : 읽기(Read)
  - `PUT/PATCH` : 수정(Update)
  - `DELETE` : 삭제(Delete)

#### RESTful Communication
  - 요청 : 클라이언트가 데이터를 헤더, URL, 쿼리 파라미터, 본문에 담아 전송
  - 응답 : 서버가 상태 코드, 헤더, 본문으로 응답

#### HTTP 상태 코드
  - 100번대 : Information
  - 200번대 : Success
  - 300번대 : Redirection
  - 400번대 : Client Error
  - 500번대 : Server Error

PS) `418` 상태 코드(I'm a teapot)는 Web 의 유머러스한 Easter Egg

![GoogleStatus418](../Media/GoogleStatus418.png)
