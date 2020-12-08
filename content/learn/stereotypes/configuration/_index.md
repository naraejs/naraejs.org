---
title: "@Configuration"
weight: 22
date: 2020-12-05T02:53:00+09:00
categories: ["StereoTypeAnnotations"]
tags: []
cover: ""
draft: false
---

# Description

단독으로 보통 사용되진 않으며 다른 Module과 함께 작동합니다.

# Usage

```typescript
import { installer, Configuration } from '@naraejs/core'

@Configuration()
class MyConfiguration {

}

export default installer;
```

# Configuration 만들기

[webserver-express의 소스 참고](https://github.com/naraejs/naraejs/blob/master/webserver-express/src/configuration.ts)

