# Title

https://github.com/type-challenges/type-challenges/blob/main/questions/00014-easy-first/README.ja.md

<a href="https://tsch.js.org/14/play/ja" target="_blank"><img src="https://img.shields.io/badge/挑戦する-3178c6?logo=typescript&logoColor=white" alt="挑戦する"/></a>

## 例

```ts
type arr1 = ['a', 'b', 'c']
type arr2 = [3, 2, 1]

type head1 = First<arr1> // expected to be 'a'
type head2 = First<arr2> // expected to be 3
```

## 解答

```ts
type First<T extends any[]> = T extends [] ? never : T[0];
```

<a href="https://www.typescriptlang.org/play?#code/PQKgUABBCMAsEFoIDECWAnAzgFwgewDMIBBddAQwE9JEE76aAjSkgO2wAs9WXkBXCAAoAAuXYE+ASggBiQLhKgLF9Z5MlTA0ZmiICuYwPKq6qIFlEwOhKAAwAqpwEkMgdeVAigyA15UBRDIEAGQLoMgOwZAAOZyPgdYZAW4ZARYZAMYZAYoYPQGj1K0AV+MBNBlM0LGwAHnMAPmtAfO1AUYjAdQZAPwY4wCAGAwhAaPlACQZABwZALH+y00bsTBpsSgAHAFMIFXRoCABeCABtAHJyUYAaCFHGKZmAY1GAXVaO7t6AJkGRgGZpzenoVbWuiA5O8gATfqGknBTe6HSIYGAIToAPLoXsTquINg8BBGN1xqNTt0LtdtncMA8ti83h9vp1fv9AcDQRBdjRGqYyi8AOKobAACT4jEA5gyALo9ALFRcUA0Qy1DjYbDtTAALjezQWHAAdAArTD8vDoADmwDgwEF5DAIGA6lAEAA+mr1Rr1RBAMoM2sA1gyAZoZAD8MgEmGKyADCjAKaKqs1tpVEAV6jaZ3uqXMKL+rCumB6PGGyxeQ3dX093pGywgAH4IKxOgA3TroCCciDmYYABmWAG4lSAbXaNRAQoBOhkAEwyARoYjcX8wW1Q7FagALbtMW4Z3dADeEAAogBHPjkAA2027qN+EAAvhACOg8I2ZsJ2wg+UPB51WOLOphgHxsKhB5gIWB2xAFuRMFudsMaKOfqk+wPBylXSlhvsIIcYAHprt0ulJjeY73v2Q7PvCqTDII0gDC80CbO+XbkCmODoKgG6Tt+QjQbB8F-gBUC3miwGPmBySvphsYJugeGAXeKQPqBL7DHwXqdAQaH-JhLFXGxHFXDRJwnoms5YFeNDIoumAIF8d7SWQYo0C+oysHg2CkBQlCjP+4nvJJ0lAXJImKeBKRdumKbjKolAADKoAA1p0oyTtpJzKrWhaAITWHjFiEgDDDH4Na1vWYCgDQLyAMeRgAq3lYgCOioAkOZMiybIctywC8gKwqihKUqwMAYiYAA7omMpylAEXRYA0ZHMqy7JcjymB8kKIpipK0qYHgg67qg3AtGVECeIAa3IeIATVGADIZSW1al6VNVlkqyvKipAA" target="_blank"><img src="https://img.shields.io/badge/解答-3178c6?logo=typescript&logoColor=white" alt="解答"/></a>