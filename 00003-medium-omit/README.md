# Omit

https://github.com/type-challenges/type-challenges/blob/main/questions/00003-medium-omit/README.ja.md

<a href="https://tsch.js.org/3/play/ja" target="_blank"><img src="https://img.shields.io/badge/挑戦する-3178c6?logo=typescript&logoColor=white" alt="挑戦する"/></a>

## 例

```ts
interface Todo {
  title: string
  description: string
  completed: boolean
}

type TodoPreview = MyOmit<Todo, 'description' | 'title'>

const todo: TodoPreview = {
  completed: false,
}
```

## 解答

```ts
type MyOmit<T, K extends keyof T> = {
  [P in keyof T as (P extends K ? never : P)]: T[P]
}
```

<a href="https://www.typescriptlang.org/play?#code/PQKgUABBDMELQQPIFsCWAXS8491gRgJ4QCCAdugBYD2ZxAYgK4QAUAAgIYUBmjAlBADEgWjlAWL5DGZVLSH5GqADbo4qMmCyDNEQFcxgeVV1UQCK+gfwZAPfHHAdgyBo9UBnDIB+GQGMMgYoZAVwzOABigwAeACoAaCABpAD53QCSGQH95QApXQG0GQC0GQEAGd193C0B1hkBbhkBFhmdAaQZASIZ3IIjAKSVAEzTATQZAaIYrcMB87UBRiMB1BkA-BkrAIAYDCEBo+UAJBkAHBm73EfQAZyxVdABTACduDgBjaYhfagATaggAbywodAwFaYAuCDH0WdUAcz2IdemxxcuABwPaU-PLshuoKEXqZDPI4zdanfDUahHLhYAC+3XQhGeKzWmwACrNpgA3VDTADuEAAvBAALKELzoPwbaiBADk90eLzeZBpEAAPhAaQd0EcaSFuv8yOcIOgqacUdR0VicfiibtfhB-oDgdNQRAFgoxtN-LCsCN3N0QhAAOIYAASjHwgHMGQBdHoBYqJqgCx-yjodDPMbHYDAcaLSgAOgAVmNfdRZldgNBgP6OGAQMB1KAIAB9ZMp1MpiCAZQYM4BrBkAzQx2QCTDOFABhRgFNFJNpyuJiCx9QIpEksloCkBYIQaYADxmZHWYwgAGtpoRqNxVobZVgANqoiCqAdDkerCAcPssGed7u9tsAfggZCxcwgp1RfAAumLp6ewHCwAmq5WIA5AJ0MgAmGQCNDHYnxX7+na6hASG6DCoiKzbBAACiACOjAcAogTgR2SKLEBMJqrMAIcmw9bTHAPqwUc3wPMAjAHBqNJ1iBCorg8hIQJOWAIUhFJQTBCjeIx0zISqACMgSkuSlKbLS9JPKgrzSMyIRSdqUAcch7HQbB7GIZxIIAEx8U2PjisJDyieJtAsuyNKKkC0wgry0lgFet7ABAWFjHAnZMU5szobMYDYe2bkhrR-HNoJ1IciJjISUZHKqJisGoOsvLqFMcwLMsqxUjsWBckcHwXNcWAhWJTJZV8PwKgCZkgmCEJQmoN4JfMSwrHJILcWl+yHCcZzZd8WCmcqqrgpC0zQjVFCJfVEEqVx6xqS1wptYVOU3neP7poAhNYWE+DiAMMM6TfstNZxqAWCGoAx5GACre4SAI6KgCQ5o6zquu6nren6gbBqG4bAFwYy4nMkbRlAJ3nYA0ZHVE6Lpuh6XqPM9QYhmGEZjJCJESRM-0QIAugwWIAa3IWIATVGADIZoP3RDT0BjDb1RjGcZAA" target="_blank"><img src="https://img.shields.io/badge/解答-3178c6?logo=typescript&logoColor=white" alt="解答"/></a>