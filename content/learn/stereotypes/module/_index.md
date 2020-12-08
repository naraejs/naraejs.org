---
title: "@Module"
weight: 21
date: 2020-12-05T02:53:00+09:00
categories: ["StereoTypeAnnotations"]
tags: []
cover: ""
draft: false
---

# Description

Module를 만들 때 사용합니다.

# Module 만들기

```typescript
import { INaraeCore, Module } from '@naraejs/core'

const S_MyModule = Symbol('MyModule');

@Module()
export class MyModule {
  private _core!: INaraeCore;
  
  constructor() {
    makeToModule(S_MyModule, this)
      .order(0)
      .start((core: INaraeCore) => {
        // START Handler
        this._core = core;
      })
      .stop(() => {
        // STOP Handler
      })
      .build();
  }
}
```
