---
title: "@ConnectionManager"
weight: 30
date: 2020-12-05T02:53:00+09:00
categories: ["StereoTypeAnnotations"]
tags: []
cover: ""
draft: false
---


# Usage

```typescript
import { installer, ConnectionManager, IConnectionManagerHandler } from '@naraejs/core'

@ConnectionManager()
class RedisConnectionManager implements IConnectionManagerHandler {
  public get name(): string {
    return 'redis';
  }

  /**
   * If false, the entire health check is not affected even if the health check fails.
   */
  public get essential(): boolean {
    // false이면 해당 ConnectionManager의 Health가 DOWN이라도
    // 전체 Health Check에서 DOWN을 반환하진 않습니다.
    return true;
  }
  
  /**
   * If true, transactions are automatically processed when Transactional Annotation is set.
   */
  public get transactional(): boolean {
    return true;  // transaction supported
    return false; // transaction not supported
  }
  
  /**
   * If successful, resolve the Promise and return details.
   * If failure, reject the Promise. see {@link IHealthCheckError}
   */
  public healthCheck(): Promise<any> {
    return Promise.resolve(); // Health is UP
    // or
    return Promise.reject(...); // Health is DOWN
  }

  /**
   * TransactionalConnection
   *
   * If transactional is set, must implement {@link ITransactionalConnection}
   */
  public getConnection(): Promise<TConnection> {
    // ...
  }
}

export default installer;
```

