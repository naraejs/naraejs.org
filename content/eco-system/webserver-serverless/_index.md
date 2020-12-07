---
title: "webserver-serverless"
weight: 30
date: 2020-12-05T02:53:00+09:00
categories: ["EcoSystem"]
tags: []
cover: ""
draft: false
---

<div class="no-color-anker" style="font-size: 1.5em">
    <a href="https://github.com/naraejs/naraejs"><i class="fab fa-github"></i></a>
    <a href="https://www.npmjs.com/package/@naraejs/webserver-serverless"><img src="https://img.shields.io/npm/v/@naraejs/webserver-serverless.svg" /></a>
</div>

# Installation

```bash
$ npm install --save @naraejs/webserver-serverless
```

## Basic Code

```typescript
import * as naraejs from '@naraejs/core';
import * as webserverExpress from '@naraejs/webserver-express';
import * as webserverServerless from '@naraejs/webserver-serverless';

naraejs.install(webserverExpress);
naraejs.install(webserverServerless);

/**
 * YOU MUST CALL createHandler BEFORE narae.js START
 */
const app = naraejs.create();
const handler = webserverServerless.createHandler(app, webserverServerless.ServerlessPlatform.KUBELESS);

app.start();

export {
  handler
};
```

# Supported Serverless Platforms

## Auto

```typescript
const handler = webserverServerless.createHandler(app, webserverServerless.ServerlessPlatform.AUTO);
```

* AWS Lambda : `LAMBDA_TASK_ROOT` Environment가 있는지 확인합니다.
* Kubeless : `KUBELESS_INSTALL_VOLUME` Environment가 있는지 확인합니다.



## Kubeless

```typescript
const handler = webserverServerless.createHandler(app, webserverServerless.ServerlessPlatform.KUBELESS);
```

## AWS Lambda

*NOT TESTED*

```typescript
const handler = webserverServerless.createHandler(app, webserverServerless.ServerlessPlatform.AWS_LAMBDA);
```
