# Includes

https://github.com/type-challenges/type-challenges/blob/main/questions/00898-easy-includes/README.ja.md

<a href="https://tsch.js.org/898/play/ja" target="_blank"><img src="https://img.shields.io/badge/挑戦する-3178c6?logo=typescript&logoColor=white" alt="挑戦する"/></a>

## 例

```ts
type isPillarMen = Includes<['Kars', 'Esidisi', 'Wamuu', 'Santana'], 'Dio'> // expected to be `false`
```

## 解答

```ts
// MyEqual: https://zenn.dev/yumemi_inc/articles/ff981be751d26c
type MyEqual<X, Y> =
  (<T>() => T extends X ? 1 : 2) extends
  (<U>() => U extends Y ? 1 : 2) ? true : false
type Includes<T extends readonly any[], U> = T extends [infer First, ...infer Rest]
  ? MyEqual<First, U> extends true
    ? true
    : Includes<Rest, U>
  : false;
```

<a href="" target="_blank"><img src="https://img.shields.io/badge/解答-3178c6?logo=typescript&logoColor=white" alt="解答"/></a>