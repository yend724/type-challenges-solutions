# Unshift

https://github.com/type-challenges/type-challenges/blob/main/questions/03060-easy-unshift/README.ja.md

<a href="https://tsch.js.org/3060/play/ja" target="_blank"><img src="https://img.shields.io/badge/挑戦する-3178c6?logo=typescript&logoColor=white" alt="挑戦する"/></a>

## 例

```ts
type Result = Unshift<[1, 2], 0> // [0, 1, 2,]
```

## 解答

```ts
type Unshift<T extends unknown[], U> = [U, ...T];
```

<a href="https://www.typescriptlang.org/play?ssl=21&ssc=50&pln=21&pc=1#code/PQKgUABBDMAMBssIFoIFUB2BnAFgSwDMAXSFZci0gIwE8IArPAQwwHNcWIAKAAUZfY4WAWwCmRJgEoIAYkC4SoCxfWUwBOKpjTCkZOiICuYwPKqWqAAMzAQTUaAdAFds+YmZOA7BkDR6oAWGQD8MgDoZA5wyAzwyASQyA+dqAoxGA6gyAfgyAmgyAQAzGEIDR8oASDIAODIBY-4nORDQADqJYAMYqeHkkULkFEABKhbYANkQQALzoDoREADwA2gCMADQQAEwAukOwAHwQwMAQPbBDgyMDo6TOidMA4nhEABK2VIDmDIBdHoCxUTGA0QwZOEREeVgAXLNExTjW9FjWAPYqrMBwRDAehMMAgYBaUAQAD6sLh8LhEEAygxIwDWDIBmhi8gEmGIKADCjAKaKMIRxOhEHBWiqonauE6XQAKhBRAAPIiiDAAEywEHsAGsMN8AO4YHrjdDTNo9NBDawyumjADckJARJJ8IggDGGQCdDIAJhkAjQxeTUq1WwskQvDCPK-ZqUiAAbwgAFEAI62JgNIYOpkFIrNAC+EAIKm+wggAHIeJTkEUhA0GmzWIVgLYiHgGlhQxT8lSikwsIVWvNSJ7vd1na6Gl1MDTiL1RX1JkN+qNJg2i17RD6umW3ZWOjX+kMxhMG-NFhBlmMWwM2yWuy6e1XHN0eqG+qHB0NQ9BQ6KqN9vnGWCOenuD6IWJu1xuw9vm621mAoca1YBCaxcmvVgGGGQDrDEbjabH3AKBpkAY8jABVvIJAEdFQBIcyuG47geZ5gFeaMPi+X5-kBWBgBYLABVEFRgVBYCIHAoJAGjI65bnuJ4XjeNCfj+AEEGwrAD2TPBvmwUhpkAXQYXEANbkXEAJqjABkM+CaKQlD3k+Rj-hBMEISAA" target="_blank"><img src="https://img.shields.io/badge/解答-3178c6?logo=typescript&logoColor=white" alt="解答"/></a>