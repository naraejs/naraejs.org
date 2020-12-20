---
title: "Narae.js"
date: 2020-12-04T21:26:24+09:00
categories: ["home"]
tags: []
cover: ""
draft: false

---

narae.js는 node.js 플랫폼에서 제어반전(IoC)를 목적으로 하는 [bean.ts](https://github.com/jc-lab/bean.ts) 기반의 node.js 오픈소스 프레임워크이다.


# 이름

"나래"는 "날개"를 뜻하는 순 우리말의 문학적 표현이다. 불필요한 개발을 줄여 비즈니스 로직에 더욱 집중할 수 있도록 하여 개발에 날개를 달아 준다.

## 설치

```bash
$ npm install --save @naraejs/core
```

# 특징

## 의존성 주입을 통한 제어반전

[bean.ts](https://github.com/jc-lab/bean.ts)를 통해 의존성 주입(DI, Dependency Injection)을 구현하여 제어반전(IoC, Inversion of Control)을 구현한다.
Bean생성을 위해서는 [Stereo Type Annotations]({{< ref "/learn/stereotypes/" >}} "Stereo Type Annotations")을 참고한다.

## 관점 지향 프로그래밍

= **AOP (Aspect Oriented Programming)**

Java의 Annotation과 유사하도록, Javascript의 Decorator를 이용하여 AOP를 달성합니다.

다음과 같은 Annotation를 통한 AOP를 지원합니다:
* `@Slf` 어노테이션을 통해 손쉽게 logger를 사용할 수 있습니다.
* `@Transactional` 어노테이션을 통해 트랜잭션 영역을 지정해 자동으로 commit/rollback을 할 수 있습니다.

## 관점 지향 프로그래밍

= **AOP (Aspect Oriented Programming)**

다음과 같은 AOP를 지원합니다.
* `@Slf` 어노테이션을 통해 손쉽게 logger를 사용할 수 있습니다.
* `@Transactional` 어노테이션을 통해 트랜잭션 영역을 지정해 자동으로 commit/rollback을 할 수 있습니다.

# 라이센스

Apache License 2.0 을 따른다.
