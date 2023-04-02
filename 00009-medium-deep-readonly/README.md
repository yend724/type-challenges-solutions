# Deep Readonly

https://github.com/type-challenges/type-challenges/blob/main/questions/00009-medium-deep-readonly/README.ja.md

<a href="https://tsch.js.org/9/play/ja" target="_blank"><img src="https://img.shields.io/badge/挑戦する-3178c6?logo=typescript&logoColor=white" alt="挑戦する"/></a>

## 例

```ts
type X = {
  x: {
    a: 1
    b: 'hi'
  }
  y: 'hey'
}

type Expected = {
  readonly x: {
    readonly a: 1
    readonly b: 'hi'
  }
  readonly y: 'hey'
}

type Todo = DeepReadonly<X> // should be same as `Expected`
```

## 解答

```ts
type DeepReadonly<T> = {
  readonly [key in keyof T]: keyof T[key] extends never ? T[key] : DeepReadonly<T[key]>
}
```

<a href="https://www.typescriptlang.org/play?#code/PQKgUABBCcELQQCIFNkAcICVkEMAmA9gHYA2AnpPHNTZQEZkQCCRALgBbGMBiArhAAoAAjjYAzXgEoIAYkC0coCxfWQCdchUoxkE6AK2QBjVnADWyMgGdZeVGjCUZDiICuYwPKqdqICqGQGsMgDoZA5QyA9QyAEwyAdgyAmgyAngyAZgwhgIsMgJcMgIcMgD8MgP0MyYAQ-4BSDIARDIDODIC6DCGArQxe3v7BgEkMgLGKgAx6gCFugNYMgJD-lYC1UYD+DIBryoBRDIBAOoAUro1hgNEMAAYo6Nj4xOQAPAAqAHxjlYD52oCjEYDqDIB+DGGAQAzuEIDKDCGATVGAMhmA5gyA9gzlgaEdlYCORoDGDFGAIgwjgBYMgM8GgFnaWyigHkGQAGDIBVBg++0AsomAdCVAIAMgCLUwAOpvCAvFAJ0MgCsGQCWDDdAMABgDtDUaAUf1AIGRN0AQgw9HaAbQZAMkM+y2gGkGLbwwD3yoBfgKxgAU0nqADctAKAMWMAjQzJDGVQDVDIAFhmSo2O3yu8MAV4GAMCVlYBquMagERjQBkRvLvoAZBiugFkGPaHSiAaPlABIMgAcGI5jR2scyUVhkNDICAADQgAF4IABvShQAAeAC5A8GoBAcBGAIxRqB0CMAcnYAEsU1GAL5Rsip9hmLNQXOu92egCiIY9hmQeD9kejEFUMw0EHDjabzbUs0YsYgCa73db5AgyYgaczOajLfUo-zE8LZGLEFLUDdHogCwIhAbkzQ0znZDmXqWEGAwAg5k4vBI9bonvMOAAtp6cJYxlWa6w62NKI6-0oM8AHF01YAAJXg6CuQAuj0AWKjRkALH-2FYVg0HMMML2dfR2AAOh0cxcIIZQAHNgGgYAdBwMAQGAOxQAgAB9ZiWNYliTmORpAGaGZJAEmGSpAAwowBTRSYtixMYiBaLsDdPX3Q9e0WM9-SDKBZ17CAAG1TEYdMiAgbSCDELcAF0IwMoyFi0sxjIgZAQx-Ig8EsIhkAAN2QZQIAAfi3KyyBsiM5J7DRFj84yljAUsGPEsSIEAMYYMSCMUMVEmL2Kk9NnzQYjWAgGTAwgCsAEdeBwEgABpCurAxcuzCAxGUAhnwnIQZLgHCypIZAiBI5BzGAXhWHTEhzCzMB8v0d8+obDTKC-Gq5mK0qSDmIKR2PL04yWSr5trPAtu2ubqsMRaSrK1abHkkKvQAJm2qrvzrO7DuM6Ty29OMGxUmMIwEaRfTPG6bvoCNzFYZRdJIyh9Ajb6oDwCM6AIAgutEKNkFhxMIBIzGhygdhcbxqB0wjcHeGQLGmx0VMwYhnqVyHXMieMAtkBIEgCAZ6Mma7EgI1monJxTcrKc7Inn35tMi1eonsxFocZe5yhc1LfLbq+n6r3ByHVwgAAfArxyIXhnwfTzVfe3af32r7KDUtt+z+v1AeB1TgtHcdachu33cYGGxeHI8IARsdkdRogZ192zCabe3RxxgPY6jgnE67OOdNJ5RydFt31ogamJy9+nRZ5od0-01n2c5rHS+jcu+cD9SBbxoX5bxuG8fLiXG7bDSpeXRXGbbptB9XZXIrezcraejXy-7IuSN1g2Ax7j2I2N02PLHsBorS9jAEJrEIMTiwBhhkAdYZUr3yS6NAICIEAY8jABVvSpAEdFQBIcyQlC0IwrDzBw-DCLETIhRUQ5gADuHlKLUSgGeJ+lRADRkSMZCqF0KYWANhPCBEiKkXIsAcwKNBrpmIC6GBEAiiADW5c4FxkHfzQRggB2CyJURonRIAA" target="_blank"><img src="https://img.shields.io/badge/解答-3178c6?logo=typescript&logoColor=white" alt="解答"/></a>