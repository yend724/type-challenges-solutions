# Promise.all

https://github.com/type-challenges/type-challenges/blob/main/questions/00020-medium-promise-all/README.ja.md

<a href="https://tsch.js.org/20/play/ja" target="_blank"><img src="https://img.shields.io/badge/挑戦する-3178c6?logo=typescript&logoColor=white" alt="挑戦する"/></a>

## 例

```ts
const promise1 = Promise.resolve(3);
const promise2 = 42;
const promise3 = new Promise<string>((resolve, reject) => {
  setTimeout(resolve, 100, 'foo');
});

// expected to be `Promise<[number, 42, string]>`
const p = PromiseAll([promise1, promise2, promise3] as const)
```

## 解答

```ts
declare function PromiseAll<T extends any[]>(values: readonly [...T]): Promise<{ [K in keyof T]: Awaited<T[K]> }>
```

<a href="https://www.typescriptlang.org/play?#code/PQKgUABBBMAMEFoIAUBOB7AtgSwM4FMA6AQwBtTJEFqbKAjATwgEEA7AFwAt1WmAxAK4QAFAAFiHAGYCAlBADEgWjlAWL4LiqVMSbyADhhwEwleSYiArmMDyqkahosefBECXDIBKGQPUMgKwZAVQyA1hkAdDIHKGV0AJhkA7BkBZRMB0JUAkhkB15UBFBkA15UBohkAi1MAHUwgAA1sDfGZyTIhAawZAaPUowA25OMAzBkB5BkADBkBVBkARBkAgBkBuI0AohkASBUB7Biyc+wAeABUAPkLAcwZAIQYkwFH9QEDIwBkGKY7APwZATQYWwGUGLYnAQAZM4cKewGPIwC8bBsAYhkB9BkAFX0Ac83CIic3rLMzM9lxKAGMeXHYED0dgIAEYIABeFD6eyEVD4XDoUgAN3wwgAzDIANy-f6A4G5aCQiAAFmgOKgf1YAKBMII6OJrHwAHdoSD8IMAahsKwAOajYTCeGIlH4AA0EHhACt8D92HIIaMIABvShQAjsYbYTD4dACdhChFI1ES0GwWASgDkknQ6Et2MoAF8HZRgMAIPgAB46WXsfAAEwg7HQEDoDmydI5AG1WAJMGHUBKyRKuTzeQBdca46n44kDAj5UjCKME+ygiWlgjQCuR9HpiDEXAQKkAmSUD6ZN5KgDi2HYAAkBHQJoAuj0AsVHrJKALH-OOx2DpcAAuN1fH6cQhS3CEdCoXnAODAKXEMAgYBGUAQAD615vt5vEB2RUAzQyAH4ZAJMMUUAGFGAU0Ur3f-5eECnkY-qyqQ6gONIrBytgPBsrkhYjB6np+qw-pNhIDBRpmwjImQAgIoukr4MQ-o8KQTBRoQ1HDOmMhEfmHLKhAUYANIQDyEAANb4Aw6CSBAtFEcwzLEH2AYjGxmYQI6ozniAf4AbeECAGMMgCdDEEgCNDC+amKUp15AWe2o6DugLsAwPoqhAACiACOAhkBK1ner6MkQJI+gQJaojmT6CBrmQpD4HyCLAPq2CkLglpGC2+KRoWwwIuw4JQoxhbFuWMASnWDZNrFbaxbS7IJUlRKpfF5AZRK1bwbCwrGmimL1o2zZ4gVeJFQh5CJQCDLlcVlVRplNWMXCRqihiMh0WAhWVnk3VJSSeYVaQgzMBoWiDLG8b4KgEAAD61QQW1xgmoznVVWUQHWbZgL5Dg-I2CLElGlDOT6cqDHZDmrfd-GdfYJUApljGDEN1XZZm51im9Lmfd9ZCDH9AlzUD7AjZGYPDRK20JlDoww1A72+l99mI8jAMFgtvUSqDManbtOMM4mEC47t+OEzZcPsKTP1IxZuooytPXsCStOY2zqDYedBNgOm8l6fpECAITWIRqSpgDDDIA6wyK0phlgKAlBKicgAq3lEgCOioAkOaTjOc4LsuwCruum7bru+6wMAEi4Myu2HseUDG2bgDRkdOs7zkuK64GuG5bjue4HiK4X-EbECALoMISAGtyISAE1RgAyGbb4cO07Meu3uR4nmeQA" target="_blank"><img src="https://img.shields.io/badge/解答-3178c6?logo=typescript&logoColor=white" alt="解答"/></a>

## 関連

- [Awaited](../00189-easy-awaited/README.md)