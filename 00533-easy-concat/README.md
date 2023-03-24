# Concat

https://github.com/type-challenges/type-challenges/blob/main/questions/00533-easy-concat/README.ja.md

<a href="https://tsch.js.org/533/play/ja" target="_blank"><img src="https://img.shields.io/badge/挑戦する-3178c6?logo=typescript&logoColor=white" alt="挑戦する"/></a>

## 例

```ts
type Result = Concat<[1], [2]>; // expected to be [1, 2]
```

## 解答

```ts
type Concat<T extends unknown[], U extends unknown[]> = [...T, ...U]
```

<a href="https://www.typescriptlang.org/play?ssl=21&ssc=69&pln=21&pc=1#code/PQKgUABBCsDMsQLQQMIHsB2BjAhgF0iUWJMICMBPCAQQwBMAnAUyoGkGcBnNAN04GsqACgACZZrAAM-DgDYAnFk4BKCAGJAuEqAsX3U4GHCmEJqTEQFcxgeVUjUAFI4eOAMpYGASwAOeCIDsGAAbV9HAoAOixMXDxfQCLUwAdTQCSGQGj1QHaGQE6GQDGGQAOGQGsGQHztQFGIwHUGQD8GQE0GQCAGQGUGbwTAewYIACYIQBMGb0BUfXjAdeVARQZANeVAKIZAQAZunsBjBkB9BkAShjTAG4ZAH4ZAfoZvQEDIwAJfOMAwDKzAahVAAIZABtMCwBEGQFlEwHQlOMAV+OLy6whAaPlACQZABwZALH-b3w+8TkI8CncmCAAJSYnAArgAbLwAXlQ4XwAB4ANoARgAugAaCCI+qogB8AG4IMBgBAmAAPf5YPBMOgQPBoCBkAEozE4wgfXy3XEQADirjwAAlQWRAOYMgC6PQCxUSVANEMLwAFng8O5OAAuYlfLBy4IAK04wTQDAA5sA4LBgNqcGAQMAjKAIAB9R1O51OiAVCpZQDNDLNAJMMcUAGFGAU0UHS7Q-aINajL9-rDsAiACqksnU+icCCgjD8DBoADuGERGIgAFUkym6GmM1nc-m8RAYYjgo345jG8Ei6jbSAQ2HnRA0ilABMMgEaGWYpbs9x0Rm2uAC27gNXmjAIA3hAAKIAR1BOHBmLXFKYVIgAF8IAAzBhoGcQADkIiXiE1O-BTAwhpBwFBeFc4M4N6jfwArgnAgnWWKEPulJ4PCm7buC8LoHG0EFpiBa4qheLoRBB5UjBW47ghcLIYWKJ4qhaK4lhUCQYe0GwQRiEREiyKsiRsCYgALGRWIsQ0mLsRAXGUei2FQXhcGEUhSI3siN6spiN6wDeJFnjuIGYmQaBoC+OAYApHHKehWIyXJfG3kpmKqb+TAaVpOl6beBmYSJHZgHaE69oAhNbeOkgDDDIA6wzjhOU5ueAUDcoAx5GACrecSAI6KgCQ5jK8qKsqarABqWq6vqRomvAwC6ZwOZMAw5qWuFEDRXEgDRkbKCpKqq6qcJqOp6gaxqmsA3Dgl+riYN85WALoM3iAGty3iAE1RgAyGcl9VpRlLXZcaFpWjaQA" target="_blank"><img src="https://img.shields.io/badge/解答-3178c6?logo=typescript&logoColor=white" alt="解答"/></a>