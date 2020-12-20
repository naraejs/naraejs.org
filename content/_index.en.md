---
title: "Narae.js"
date: 2020-12-04T21:26:24+09:00
categories: ["home"]
tags: []
cover: ""
draft: false
---

narae.js is a node.js open source framework based on [bean.ts](https://github.com/jc-lab/bean.ts) for the purpose of control inversion (IoC),

# Name

"Narae" is a literary expression in pure Korean, meaning "wing". It gives wings to developing by reducing unnecessary development and allowing more focus on business logic.

## Installation

```bash
$ npm install --save @naraejs/core
```

# Features

## Inversion of Control through dependency injection

Implement DI through [bean.ts](https://github.com/jc-lab/bean.ts) to implement IoC.
For bean creation, refer to [Stereo Type Annotations]({{< ref "/learn/stereotypes/" >}} "Stereo Type Annotations").

## Aspect Oriented Programming

= **AOP**

Similar to Java's Annotation, AOP is achieved using Javascript's Decorator.

AOP is supported through the following annotations:
* easy to use logger through `@Slf` annotation.
* automatically commit/rollback by designating transaction area through `@Transactional` annotation.

# License

Apache 2.0
