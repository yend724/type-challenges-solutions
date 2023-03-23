# Readonly

https://github.com/type-challenges/type-challenges/blob/main/questions/00007-easy-readonly/README.ja.md

<a href="https://tsch.js.org/7/play/ja" target="_blank"><img src="https://img.shields.io/badge/挑戦する-3178c6?logo=typescript&logoColor=white" alt="挑戦する"/></a>

## 例

```ts
interface Todo {
  title: string
  description: string
}

const todo: MyReadonly<Todo> = {
  title: "Hey",
  description: "foobar"
}

todo.title = "Hello" // Error: cannot reassign a readonly property
todo.description = "barFoo" // Error: cannot reassign a readonly property
```

## 解答

```ts
type MyReadonly<T> = {
  readonly [K in keyof T]: T[K];
}
```

<a href="https://www.typescriptlang.org/play?#code/PQKgUABBDsELQQEoFMCGATA9gOwDYE9J44TSiAjfCAQWwBcALHKgMQFcIAKAAVXoDM2ASggBiQLhKgLF8x5NgEtcdOHOxiATmix4qozOQBWyAMZKA1snwBnMEVF2IgK5jA8qo2ogEV9A-gyAe+I+A7BkDR6oBnDIA-DIBjDIDFDIBXDBEABigYOAQAPAAqAHwxgEkMgP7ygBSugNoMgFoMgIAMMSkxEL6AmgyAngyAZgy+gOsMgLcMgIsMEZmAtVEegGvKgFEMgEA6uYDWDFWA0Qz+mYD52oCjEYDqDIB+DFWAQAyzgKoMgDEMgPoM-k1tEYD2DICxioBOSn2Ayvp1gOYMgLIMC-mAyQzLrhCA0fKAEgyADgyAWP8vMf90axQFR0ZBqfioIzICApTBYCAAbyIUDocjouGQAC4IJY6GoVABzZEQdDISxGfEAB1ROGxuPx2CJUAAvi8jDhcRA6HDMNiALL4eJaZKwrBpCAAXkRxNR6KxEAARAAJCwKgA0xNJ5KpNOw2IV-EwelQagVRFZRG5WAAdLKMZLFSrcLhMAqIMBgBAAKJqNSYNTYox8bCYOgQDSoSyWOQE1SocOaRJUSl+ylguiEFE861ailyalyHAOhXkE0sI1uj3e33+wPB0MJyPR2MQeMR4XJ1PpzMQf4xF7igDiaKVbHIV0AXR6AWKjxt8GHQ6JTLJiPYCjAxrfpLNb-QTgNBgPpUGAQMAbKAIAB9a83283iCAZQYH8NAM0MwUAkwyZQAYUYBTRSvd4Ay8IFPGwMzTCABSFJNUnFKUkSgdskwgABtABpCAVAgcx8EwfgYQAXWxFI0PwgBuMALQvQCAIgUJAE6GQAJhkARoZgjo-9qPvEC5AAW0pf0wzA6EEW9ABHNhUFwNVvQADzTEwIGZCB+D9biIAAcm4QS4HXCSMUZMlgDYVFcEsNTQPwcCg0sMkHWQogvVk4w6CSL0xIkpJIMTbRUh5ABGNIpKg7zRUwfy0gCsB8JsEEwQhKEYT86UUTRDE6TxQkiFzHVCz1HF0sZIh2V4jFQXQbFyCNDE+CIbjkDoVBsXgqBWyMpgAzyhkmQUijzxAdiOKAwBCa18OjQkAYYZGn6jjgLPUAiHFQBjyMAFW9MkAR0VAEhzWd50XZdV3JDctx3NQ9wPPhLAAdzBQ9jygRaVsAaMixjnBclxXYA1wO7dd33YBLEwXAjJyoEIHFQBdBl8QA1uV8QAmqMAGQznp2t6Ps3L7juuk8zyAA" target="_blank"><img src="https://img.shields.io/badge/解答-3178c6?logo=typescript&logoColor=white" alt="解答"/></a>

