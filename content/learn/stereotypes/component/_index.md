---
title: "@Component"
weight: 10
date: 2020-12-05T02:53:00+09:00
categories: ["StereoTypeAnnotations"]
tags: []
cover: ""
draft: false
---

# Description

특별한 기능은 없는 Singletone Bean Object를 만들기 위해 사용합니다.

# Usage

```typescript
import { installer, Component } from '@naraejs/core'

@Component()
class MyComponent {

}

export default installer;
```
