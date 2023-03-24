# Title

https://github.com/type-challenges/type-challenges/blob/main/questions/00018-easy-tuple-length/README.ja.md

<a href="https://tsch.js.org/18/play/ja" target="_blank"><img src="https://img.shields.io/badge/挑戦する-3178c6?logo=typescript&logoColor=white" alt="挑戦する"/></a>

## 例

```ts
type tesla = ['tesla', 'model 3', 'model X', 'model Y']
type spaceX = ['FALCON 9', 'FALCON HEAVY', 'DRAGON', 'STARSHIP', 'HUMAN SPACEFLIGHT']

type teslaLength = Length<tesla>  // expected 4
type spaceXLength = Length<spaceX> // expected 5
```

## 解答

```ts
type Length<T extends readonly unknown[]> = T["length"];
```

<a href="https://www.typescriptlang.org/play?#code/PQKgUABBCMAcEFoIBkCmA7A5gFwBYQHsAzCAFQFcAHAG1UkQUafoCMBPCAZwEt0CD0EABQABHnwEBKCAGJAuEqAsX1nYqtMPRmaIgK5jA8qrqogfoZA6wyBrhgAGpc4CSGQOvKgRQZAa8qAohkCADIF0GQHYMJ058DuqYCqDNaAK-GAmgyA0ermaFh4ADykAHw2gPnagKMRgOoMgH4MoYBADAYQgNHygBIMgA4MgFj-+eZV2Jz02GyUqBDYqJzUAIYQALwQANoA5C1t7f0ANBD9ALYEACao1BAAzGMT03MLABorU7PzEACa-QC6dQ1NnJTtAMaoG919-QBiAILIAMIA8gByEACc2y93t8IAAJACizwAaodxv0ACIAJWeAHFvtsAMqkZ4I9EggCSAAVtiCAKoAWWeP3RBOebzBj2QeORINIx3y9UazVaHWiOHwPV5cSGHQSUGAwAgqAAHo0ri0ZhAACynTkXa63QX8lAYPmxNU3Dai8WSmWoOWoBUAVnoVXM+VFyO42BB5BYgHMGQBdHoBYqNCgGiGMq4bDYSicABc4pqV1wADoAFacaMEABOmGAcGAsfaYBAwHUoAgAH0i8WS8WIIBlBnLgGsGQDNDIAfhkAkwzWQAYUYBTRULpc7BYgOfUHKamviJpa6BmnAgSdQ7RmAmoHHI6AA1nwAO7oXpHUU9Ui9ABEtBiuF3RwA3HmQB2uyWIIAxhkAnQyACYZAI0Mdbvl6vRZ7ue4k0oyewzRnBAADeEBggAjuQ7TUOMYKmnKEAAL4QEQSYEJMEwiP2CBRtBB6YK0wDkNg3DUJw-TqFcAicABwqdD0Ax0dsax7MssIsZszG7AshxHBA7TjlR6A0WAQk0VwlwGvcAyAp8Pz-LCsnAuCUIwhMiIomisKYtiuKEsS5KUhA1K0vSjLMqyfECRAYnYH2QFXAJrTSfQcGytgsQQVB1CxIO-bEFywwJOMioJMFrnwR5XnQb5OpCmcAX6rcwUQJaYWjPQxpYZwCDSu5uVJmhSb0IOaUZWKErZblkUFUVJVxbgsT9Lg8zUAQEArsm1AzP04UnGA+YftegCE1p4d43oAwwzGO+H5fgN4BQKKgDHkYAKt7WIAjoqAJDmfoBkGIbhsAkYxvGiYpmmsDAO0wkrqgSYZlmi0QKt1iANGR-qBsGYYRpwUZxgmyapumnAENQxHcNR9Cil4gBrcp4gBNUYAMhm7Z9B1HX9p2ppm2a5kAA" target="_blank"><img src="https://img.shields.io/badge/解答-3178c6?logo=typescript&logoColor=white" alt="解答"/></a>