---
title: API Type
---

### 1 . 1 . 1 API Type

#### 각 **API** 는 다음을 정의

- **Protocol** : Control structure
- **Format** : Content structure

#### **API** 종류

<ol>
  <li style='font-weight: 900'>
  <span style='font-weight: normal'>초기 <b>API</b></span>
    <ul>
      <li style='font-weight: normal'>주로 Local Libaray Function 호출 형태</li>
    </ul>
  </li>
  <br>
  <li style='font-weight: 900'>
  <span style='font-weight: normal'><b>원격 프로시저 호출</b>(RPC)</span>
    <ul>
      <li style='font-weight: normal'>다른 Process 나 Computer 의 Function 를 Local Function 처럼 호출</li>
      <li style='font-weight: normal'>Ex) gRPC<sup id="grpc-ref"><a href="#footnote-grpc">1</a></sup></li>
    </ul>
  </li>
  <br>
  <li style='font-weight: 900'>
  <span style='font-weight: normal'><b>Messaging</b>(RPC)</span>
    <ul>
      <li style='font-weight: normal'>Process 간 Small data Chunk</li>
      <li style='font-weight: normal'>Command 나 Event 가능</li>
      <li style='font-weight: normal'>Ex) Apache Kafka, RabbitMQ, ZeroMQ</li>
    </ul>
  </li>
  <br>
  <li style='font-weight: 900'>
  <span style='font-weight: normal'><b>Communication Pattern</b>(RPC)</span>
    <ul>
      <li style='font-weight: normal'><b>Request - Response</b> : Web Browser - Web Server</li>
      <li style='font-weight: normal'><b>Publish - Subscribe</b>(Pub - Sub) : Publisher 가 Message publish, Subscriber 가 선별적으로 Receive</li>
      <li style='font-weight: normal'><b>Queue</b> : Pub - Sub 와 유사하나 Single Subscriber 만 Message 처리</li>
    </ul>
  </li>
</ol>

이 모든 기술들은 Web Service 에서도 Back-end 작업 수행 등에 활용 가능

---

## Footnotes
  
<ol>
  <li id="footnote-grpc">
    <a href="https://grpc.io">https://grpc.io</a>
    <a href="#grpc-ref" title="돌아가기">↩</a>
  </li>
</ol>
