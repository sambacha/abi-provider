# [abi-provider](#)

## Overview

> TODO

## Middleware

Mddleware must implement `ABIProviderMiddleware` interface:

```typescript
interface ABIProviderMiddlewareContext {
  // an instance of ABIProvider where middleware was called
  abiProvider: ABIProvider
  // address of contract, for which ABI was loaded
  address: string
  // ABI retrieved by ABIProvider
  abi: ABIElement[]
}

interface ABIProviderMiddleware {
  (ctx: ABIProviderMiddlewareContext): Promise<ABIElement[]>
}
```
