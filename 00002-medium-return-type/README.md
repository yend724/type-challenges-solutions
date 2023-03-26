# Get Return Type

https://github.com/type-challenges/type-challenges/blob/main/questions/00002-medium-return-type/README.ja.md

<a href="https://tsch.js.org/2/play/ja" target="_blank"><img src="https://img.shields.io/badge/挑戦する-3178c6?logo=typescript&logoColor=white" alt="挑戦する"/></a>

## 例

```ts
const fn = (v: boolean) => {
  if (v)
    return 1
  else
    return 2
}

type a = MyReturnType<typeof fn> // should be "1 | 2"
```

## 解答

```ts
type MyReturnType<T> = T extends (...args:any) => infer R ? R :never;
```

<a href="https://www.typescriptlang.org/play?#code/PQKgUABBBMELQQOIFMAuEBKaCuAnAdhACoCeADspPHDbVQEYkQCC+qAFgPb5MBi2EABQABAIZsAZtgCUEAMSBaOUBYvvICW+Cclzz62VQBtUcdWCpzzEQFcxgeVVTUQCK+gfwZAPfGPAdgyBo9UBnDIB+GQGMMgMUMgFcMgQAGWKh4+KQUADxEAHyhgEkMgP7ygBSugNoMgFoMgIAMoUShboDcRoBRDIAkCp7JgGvKgOn6gJoMgNEMHsmA+dqAoxGA6gyAfgz1gEAMdhCA0fKAEgyADgyDoVOoAM5UAMbcM+gShAC8QgBuAFwQ9Jyc+sjismsJEADeVFCqElvS11AQuDgEEACMj8j6M5RPTy9Im9oFQAL6DVDkZAQUQQDYAWRIESiMWQsUhFE4d1W52AwAgMy42H0ABM9tCAETvCAAHxgFKoU1Cg3OiFUqAAEth6IBzBkAXR6AWKimoAsf-YqFQZBm2zxs3m7AAdAArGbyzi4ADmwGgwEVojAIGAplAEAA+mbzRbzRBAMoM1sA1gyAZoYfIBJhmSgAwowCmiqbLT6TRADaYMdDEciCKj4ucNkQIMgAB6oZD4EkzITytOiDVS8QkU7ndSabQYCAAfkwEG2+GQmy0AG4jSBvb6LRA-IBOhkAEwyARoYfK3G02zf7DaoALZkNXoIOXCAAUQAjthRPoADQz2MUeboUEQCS4TjDiAAcmEQbgcsXR3w6uQM2A2FQBhmB8DUIg81EvxTGwA2lRp2vkBusRzgu+ixMsuDqOqK4hq80RQrEgi5gSqAQZeCToUuv7-oBwGLrE7zQAAzNBSKweGiFwucBGEehCSYVAf7rqgQHznhADCe5kEcsYAPL0IqAGoCRoZwXEFFnBAHGjtxfECRutH0auTEsSBsQAAq7sOqi-LE+yHMc+B0RAMFAqJaLiecGl7tpaJ6Uc4i0XRWHKbhoEWYeEgHAewlkfB7nuQenmcAeCnOYJKl4dSdLQD5pnhkGWLboZGFhThrGgVFMCxSi8EJdi+DvKFAC6z4UJJnEyfxglwpcVCiLsX4ESugVeSVUD0BmuwHuw3z6MFVBkC8myIbs+DYMO9BaGA4JgIs+DLElNWCDsewHPZ+BIZsJYfOWMCzUsKwFUtK12QZK4AO67Nmm3bdSuwgmAxr9s2gCE1m4rZ+IAwwyAOsMfb9oOj3gFA5yAMeRgAq3skgCOioAkOYimKEpSjKMxykqKpqpq2riDM51aDqerAxA4PJIA0ZGNKK4qStKwCygqyqqhqWrADMhx3qoSxUOcgC6DG4gBrcm4gBNUYAMhnkwjVM06j9Oarq+qGkAA" target="_blank"><img src="https://img.shields.io/badge/解答-3178c6?logo=typescript&logoColor=white" alt="解答"/></a>