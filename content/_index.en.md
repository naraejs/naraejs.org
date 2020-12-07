---
title: "Narae.js"
date: 2020-12-04T21:26:24+09:00
categories: ["home"]
tags: []
cover: ""
draft: false
---

narae.js is a node.js open source framework based on [bean.ts](https://github.com/jc-lab/bean.ts) for the purpose of control inversion (IoC),

# README Languages
* English (this)
* [Korean](README.ko.md)

# Name

"Narae" is a literary expression in pure Korean, meaning "wing". It gives wings to developing by reducing unnecessary development and allowing more focus on business logic.

## Installation

```bash
$ npm install --save @naraejs/core
```

# Features

## Dependency Injection

= **DI**

Dependency injection is supported through bean.ts.

## Inversion of Control
= **IoC**

*There are still many things that are not enough to say that it is a complete IoC.*

In the existing express-based software, the user has to implement the router directly, and when an error occurs in the handler, 500 errors do not occur and a response is not provided.
In narae.js, a user can easily implement a handler through the @RequestMapping annotation without having to create a router.
Also, catches and handles errors that occur in handlers for possible error occurrence situations.

# License

Apache 2.0
