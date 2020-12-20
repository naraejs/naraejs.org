---
title: "Logging"
weight: 20
date: 2020-12-20T02:53:00+09:00
categories: ["Logging"]
tags: []
cover: ""
draft: false
---

# Simple Logging Facade

클래스에 @Slf 어노테이션을 적용하면 `this.log` 를 통해 Logger에 접근 가능하다.

Example:
```typescript
@Slf({
  namespace: 'your.namespace' // Optional
})
class SampleComponent implements Slfable {
  public log!: LoggerLike;
  
  public method() {
    this.log.info('...');
  }
}

```
