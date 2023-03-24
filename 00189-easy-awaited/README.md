# Awaited

https://github.com/type-challenges/type-challenges/blob/main/questions/00189-easy-awaited/README.ja.md

<a href="https://tsch.js.org/189/play/ja" target="_blank"><img src="https://img.shields.io/badge/挑戦する-3178c6?logo=typescript&logoColor=white" alt="挑戦する"/></a>

## 例

```ts
type ExampleType = Promise<string>

type Result = MyAwaited<ExampleType> // string
```

## 解答

```ts
type MyAwaited<T> = T extends PromiseLike<infer R> ? MyAwaited<R> : T
```

<a href="https://www.typescriptlang.org/play?ssl=25&ssc=70&pln=25&pc=1#code/PQKgUABBCMAcCcEC0ECCB3AhgSwC4FMATSZJM8kgIwE8IBZTAY23wCsIBlbAawHsAnTBAAUAAQC2TFqwDOPAZgCUEAMSBcJUBYvqoAO-XuOwz8qygFdsAG1xJsAOzAkVTiICuYwPKqDqAAU9BoxEBLhkAShkB6hkArBkBo9UAZBkBQxUBQZUBNBkBohgjAJIZASwZAOwZACIZAMQZAawZANeVAdP0EwBiGQAcGbMARBkBzBkB1BkBwhlzAaQZAIAZPCEBo+UAJBgrALH+AAx99Q3wAHgBRAA9McW0LfAAVam18AD5BwAsGatzowCEGJMAWDUAIFUBABiy8-PrAMwYIGbmF5dXjVJLyqrqm1o6SQf-cDISLgXvdZvNFis1hAALwQEZ+CYyXD8OwAc3WnRB0IASvgZKYrLD6NQMDgCIQpuCnlCNhBgMAIMjUbY0X9-p11hBAMoMmTcgBkMzKAYUVABhRgGi5QD2DBAANoCbBouyYCwQTD8XDYRiLAC6wgAFrhcNoZAAuBmEfAANwAdLheMBJIw5HxBMBMIQLZhbIwiEhsfjGKjtNZ8NN8PxmEYZEgAI6mfHq3i2JDQJAAFgArNxU8oaDKJFI2E6FDr9YaTQyFbhdaZKFbGPp7QXZPJBMpaglflAuQBxPAACRrtUAXR6AWKjkv1S0bTcBAYxdVbZFaBGjgHB4MBWJgwCBgA5QBAAPpH48n4887n5QDNDIAfhkAkwypEWAU0VD6fXweIDuHH6SWS8ERxksXJwksEAhgQtiEDI8K+GMAAyPATHYABmYYQDiXIAPw-lgf6UuhEDGhASwkBAe4gC+b4nhAgBjDIAnQyABMMgCNDNetEUZRR4fru2DzAIuAQN+ADe9yxkqAA0YJrIwfEAL4QEhvgQAA5KIfpIHOSqLKy+LAKY6oWDIilfqCAAaxIImM4zMuimLfgAmmZMFGOMQlISwFiEIRtimOIlCodJNmggAWg5oxOeZTlWayEAAD4QF5PlhusAXQoF0AhYi4zhRMWWWSi6IxRAlC8LwiyeklyXGCBcJCVW+C2IRwiJkhhKuRYiweSIqpop53m+fwygwlynrUANQ22LQ0lGdCjCYJGxLSiQMySbgUwiRY4x0KSOEUuMxnrOJkUYvti3TMtq2mEqG1beS-62ftEAuW5HXxX1ED+cdUBLfgUnnZdm2-jtgX3YdBUvYlH0Sd9K2TGtV0A-+qXA3lUWxUVJX4GVENfT9MMXet-3bf+gHiWD-BJaJYBanujIqVGIbLUgYZ6PwYDfkzAjEgTN2UqTmJgPu7FUYAhNaZLR1GAMMMgDrDGx7Gcfz4BdhAgDHkYAKt6pIAjoqAJDm46TuWM4yHOC4yEu-Armurq2DI6BhhuW6K6rqSANGRSQTgaU4MrO86Lsuq4IMAMglbp2CJkCiuALoMmSAGtymSAE1R-Ku2W06e0bJsrpu267kAA" target="_blank"><img src="https://img.shields.io/badge/解答-3178c6?logo=typescript&logoColor=white" alt="解答"/></a>