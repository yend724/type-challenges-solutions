# Readonly 2

https://github.com/type-challenges/type-challenges/blob/main/questions/00008-medium-readonly-2/README.ja.md

<a href="https://tsch.js.org/8/play/ja" target="_blank"><img src="https://img.shields.io/badge/挑戦する-3178c6?logo=typescript&logoColor=white" alt="挑戦する"/></a>

## 例

```ts
interface Todo {
  title: string
  description: string
  completed: boolean
}

const todo: MyReadonly2<Todo, 'title' | 'description'> = {
  title: "Hey",
  description: "foobar",
  completed: false,
}

todo.title = "Hello" // Error: cannot reassign a readonly property
todo.description = "barFoo" // Error: cannot reassign a readonly property
todo.completed = true // OK
```

## 解答

```ts
type MyReadonly2<T,  K extends keyof T = keyof T> = {
  readonly [P in keyof T as (P extends K ? P : never)]: T[P]
} & {
  [P in keyof T as (P extends K ? never: P)]: T[P]
}
```

<a href="https://www.typescriptlang.org/play?#code/PQKgUABBAcELQQEoFMCGATA9gOwDYE8IAmSeOci0gI0IEFsAXACx0IDEBXCACgAFVGAMw4BKCAGJAtHKAsXwkAnNFjyFxmKgCtkAYwZwA1snwBnMKXHmIgK5jA8qqmoRQCYMgOwZA0eqBUfUAOpgAMAKl8AWDF4A0l6ASQyAa8qA0QxeALL4KBg4BEQAPD4ANBBBAHxhgPnagKMRgOoMgH4MgJoMgEAMdhDBXoAyDIDgxoBZ2oCqDIAxDIBmDIAiDJGALBqAECqA9gyAgAy+Xk6STrVOgOsMgLcMgIsMgGMMgMUMToD+DKGAtVHr4YBRDIBAOoAUroDWDKWVtY2tnV2AVgxdAyOAWAmAHHpTCUoEabn+gDAqgBuWJ2GZUAngwdWaLVbbXaHU7nKqkQDR8oAJBkADgzVLyYhgmKAAS0YyDkglQWmQEB8mCwEAA3qQoAxcQxcMgAFwQIwMOT4gDmdIg6GQRi0XIADgycGyOVzsLyoFAtJgALYi5kMZDoNlUTCYZkCUgAX2qCuwHIgDEpmDZcQ+SXwqQpWEyAHIGUzkE6IAAfCBOgVC0Xi7BO7IQAC8NL5ruZbIARAAJQwx9J8v3C3Fi3ESiAxwTaqioORJvkK5Wq9Vs4m4IzIZNQQ2kc1YAB0UbJ4fjyFwuEwMYgwGAEAAonI5Jg5GytAJsJgGBAFKgjEZcdzsBBUHPFLaICLRyLCQx8A2LU3UwHM6v2-m5Gxtb3+0OR2OJ1OZxuF0uV2u359CDvMHu5API9mxLFVkDVdAwzNOQODJe8AHkglITEvGqEMAHFGTjDgqEAcwZAC6PQBYqLKSJACx-pgGAYEUjBZftsS0Jgm3UIwmzHblgGgYB1FQMAQGAUxQAgAB9ETRLE0SIEAZQZJJOQBmhkAH4ZAEmGUJAAwowBTRWE8StKEiA+NMA89wga1N2Ue1MiyCBkAADzVbB0CMCADHwTBBHJKCnJc8kQ3DWkoHnH8IAAbQABQgfFHMMTyfDXBzuFC6zbPsiyAH4IFCtlsGQAA3QkRAAXTZHwQryiAwH1CAADIIygEKwtXDzXOihceHimzkDshygggVLMpy8c0vywritK+t7wMsljMSUy0kyLqEvapKGrc8Mlp8byI3vPyTIIILQvC1aYrSyy2o6lKjoy7LCQK8lirAe9yqq2lNt2uqIucxrDtaxLOu6iBesJCA2WC66iuBu6B1GkBNO0sSICWQBOhkACYZAEaGeT4ehmGRN0-jcWVMdZ3GmkIFoXBcQMTJBysvcdAgcrBFHRUfV4ca4AY1Au3a7lBWADgGSrJ19PwQzJ2rBzw0C0hKephgUhJsnkBSSaf3tC0AEZskyG1lDSNXsj12shyp7QZblgxFfiba7R1rBVedVsPW9X1BTTDMcGDCmjZ0dV9clz2TdJs2ldtFWsCIO3GWZB2fVPdNA3dw3pe9jXfel2WA4VoPpodTAw+j52zzdiANYT42k+TPKBIHZmjDgazpdrx85DAQnCVHOQoMz5JrcwW2fXtr0fXxLL2dxdBg1MfE1SJEkyWz1XqrNCPWXZTkeVIGPXewZLJVXmVSFAssNQgLUdTQbAyonglp9JckLSIBf-K3Vsd+lWV+Xz2Pz23lfX-3pUwIgpqbUupz71knoSYkN8pal0gr5b8T8l4vzXltKaO0N6Bm-lKZBEAD7gXLMfYBZ8L53ShpjWGgBCaycPDJYgBhhhmBjTG2MSGkBDIAY8jAAq3qEQAjoqAEhzEi5FKLUVosAeijFmKsTkOxTiAgjAAHdCRcR4lANhnDADRkWRCiVEaJ0SFGIlibEOLACMDqXm54cRFwgIAXQYnCADW5JwgAmqMADIZAitHCNEUxfRkjFG8X4kAA" target="_blank"><img src="https://img.shields.io/badge/解答-3178c6?logo=typescript&logoColor=white" alt="解答"/></a>