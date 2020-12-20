---
title: "Transaction"
weight: 10
date: 2020-12-20T02:53:00+09:00
categories: ["ConnectionManager"]
tags: []
cover: ""
draft: false
---

`@Transaction` 어노테이션을 메서드에 적용함으로써 자동화된 Transaction 처리가 가능합니다.

트랜잭션을 지원하려면 `ConnectionManager`에서 `transactional`가 `true`이어야 하며 커넥션에서 `ITransactionalConnection`을 구현해야 합니다.

반드시 `@Transactional` 메서드 내에서 `getConnection`을 호출해야 하며, 중첩된 `@Transactional` 사용시 트랜잭션이 전파됩니다.

Example:

```typescript
@Service()
class TestService {
  private _testCM: TestCM;

  constructor(@Inject(TestCM) testCM: TestCM) {
    this._testCM = testCM;
  }

  @Transactional()
  public methodB(a: number): Promise<void> {
    return this._testCM.getConnection()
      .then((connection) => {
        connection.insert('THIRD');
        connection.insert('FOURTH');
      });
  }

  @Transactional()
  public methodA(a: number): Promise<void> {
    return this._testCM.getConnection()
      .then((connection) => {
        connection.insert('FIRST');
        connection.insert('SECOND');
        return this.methodB();
      });
  }
}
```
