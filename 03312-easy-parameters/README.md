# Title

https://github.com/type-challenges/type-challenges/blob/main/questions/03312-easy-parameters/README.ja.md

<a href="https://tsch.js.org/3312/play/ja" target="_blank"><img src="https://img.shields.io/badge/挑戦する-3178c6?logo=typescript&logoColor=white" alt="挑戦する"/></a>

## 例

```ts
const foo = (arg1: string, arg2: number): void => {}

type FunctionParamsType = MyParameters<typeof foo> // [arg1: string, arg2: number]
```

## 解答

```ts
type MyParameters<T extends (...args: any[]) => any> = T extends (...args: infer R) => any ? R : never;
```

<a href="https://www.typescriptlang.org/play?ssl=23&ssc=104&pln=23&pc=1#code/PQKgUABBDM0IwCYIFoIAUCGAnDBbApgC75YDOkKyV1FARgJ4S4CWAJgPZbMBe+LEACgACLDl14sAlBADEgXCVAWL6zmAOwBmJWYQCuABwA2+WbW3N9hZKrAUZtiICuYwPKq1qIBFfQP4MgHvj3gOwZA0eqAZwyAPwyAYwyAxQyAVwzhAAaYOATEZAA8ACoAfNGASQyA-vKAFK6A2gyAWgyAgAzRKdGA0gyAkQyA-QyA6wyA1wx+mYDTloCT3oCaDIDRDM2A+dqAoxGA6gyAfgwdgEAMLhCA0fKAEgyADgyAWP+T0SuE5FAAxuwqpIQQauzsEAC8gtgA5nAAXBC7XCrnADQQFwg3Ktq4tCSSNwBu7DYJzSEAA3gBfSaEei6IwAMW0Kg2hGY2zieFIKRhRlOAFl6OiEiRSElobD2Gp9ocQcBgBAANoXa63Qj3J4vLDnN4QD5fEgAXQoK2ikxBAHFmIQABLaWiAcwZAF0egFio7oLAAWhEIulIV1paw2aoAdAArUiGzjnYCwRDAY0YMAgYDWUAQAD67o9no9EEAygw+wDWDIBmhiCgEmGTKADCjAKaKbq9sddEEd1jJRnxhKIxNSEHwAA9iCpWKRBIbixcdS8VPR6fzpMcQRgKyDTiks7n8PnCwJi4bSzdVBosBAAEo1usViAAfiHEHe+D+JAA3M6QDG456ICFAJ0MgAmGQCNDEENyvV+6E07mLhdJw9smwRAAKIAR20GH0z1v2dhyIg4P2WHYuAgADkQjJsgBrPoYDz4KQwDaCi+ikAB1hbDsewHEcpwCEyNx3Ko7KvO8nzfFgvwQACQK1mCkLIbsEC0NgJxnJyzK0Ichj1s8+E3hgNwAQAggBX4kWRrDApRYDUXsdHcAxAhCYCIkURCSbYhAGwYKQUEMfSFBvh+hBJA+T76EkqbYHg6bJMmFJUuwaTPPSOEPM8vJEfyaR2Tp774MiBmPs+JkEmZRKWdi1l0VgdkMix7BsSozygi8PH8V+bkeVAunefphn+aZ8QWSSVmUlJkVVu5jxgIKYAukea6AITWPgbiEgDDDHUh5HieVXgFAIKAMeRgAq3pkgCOioAkOaqhqWo6nqpAGiaZoWla8AIMA9akAA7iQtr2t1ED9ZkgDRkV06qatqurAPqRqmuanILTapAxbBqI7BQIKALoMPiAGtyPiAE1RgAyGUdE2neds1XZadoOk6QA" target="_blank"><img src="https://img.shields.io/badge/解答-3178c6?logo=typescript&logoColor=white" alt="解答"/></a>