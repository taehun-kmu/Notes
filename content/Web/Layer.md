---
title: Layer
---

## 1 . 3 Layer

### Three-Tier Model

- Application 의 Size 와 복잡성을 관리하기 위해 널리 사용됨
- Term 은 다양하게 사용되고 있으므로 이름이 다르다고 새로운 개념이 아니며 오랫동안 사용되어 온 방식

#### Term

- **Web** : Client 의 **Request** 를 수집하고, `Service Layer` 을 Call 해 **Response** 하는 [[HTTP.md|HTTP]] 를 통한 `I/O Layer`
- **Service** : 필요할 때 `Data Layer` 를 Call 하는 **Business Logic**
- **Data** : **Data Storage & Other Service** 에 접근
- **Model** : `All Layer` 가 Share 하는 Data Definition
- **Web Client** : Web Browser 또는 **Other HTTP Client-Side Software**
- **Database** : Data Storage(주로 SQL & NoSQL Server)

![[Vertical Layer.md#Fig 1 - 1 Vertical Layer]]

#### Architecture

- **Web Layer** : Client Request 처리 & [[HTTP.md|HTTP]] I/O 담당
- **Service Layer** : Business Logic 처리
- **Data Layer** : Data 저장 및 접근
- **Model Layer** : `All Layer` 가 Share 하는 **Data Definition**

#### Layer 분리의 이점

- 전문성 분리
- Test 격리성
- 기능 대체 및 보완 용이

![[Horizontal Layer.md#Fig 1 - 2 Horizontal Communication Box]]

#### Layer 간 Communication

<ul>
  <li><code>API</code> 를 통해 이루어짐</li>
  <li>각 <code>Layer</code> 간 권장 <b>Data Format</b> 존재
    <ul>
      <li><b>Web Client &hArr; Web</b> : <code>JSON</code> 을 사용한 <b>RESTful HTTP</b></li>
      <li><b>Web &hArr; Service</b> : <code>Model</code></li>
      <li><b>Service &hArr; Data</b> : <code>Model</code></li>
      <li><b>Data &hArr; Database & Service</b> : 특정 API</li>
    </ul>
  </li>
</ul>

#### Design Principles

- **Modualarity** : **System** 을 독립적인 `Modual` 로 나누어 설계하여 유지보수와 이해 용이
- **Single Response** : 각 `Modual` & `Component` 를 가지도록 **Design** 해 복잡성 감소
- **Open/Closed** : `Software Modual` 이 확장에는 열림, 수정에는 닫힘
- **Reusability** : **Design** 한 `Component` & `Modual` 이 **Other System & Project** 에 재사용
- **Coupling & Cohesion** : **Coupling** 감소, **Cohesion** 증가시켜<br> &emsp; 각 `Modual` 간 상호 의존을 줄이고, 각 `Modual` 기능을 명확히 할 것
- **Simplicity** : 가능한 **Simple** 하게 **Design** 하여 복잡성 감소, 이해와 유지보수 용이
- **Scalability** : **System** 이 확장되거나 요구 사항이 변경될 때 **Simple** 하게 확장할 수 있게 **Design**

### Caution

- `Layer` 는 별도의 Program Language Modual 에 대한 간단한 Function 일 수 있으나<br> &emsp; 어떤 방법 동원 시 External Code 에 접근할 여지가 충분
- `Layer` 혼합 시 분리 어려움
- `Layer` 라 부른다고 **위** & **아래** 에 위치하고, Command 가 내려가는 것이 아님
- 얽힌 Code 는 Test 와 이해의 어려움 증가

[^problem]: 문제를 해결하기 위해 시도한 새로운 문제를 일으킨다
