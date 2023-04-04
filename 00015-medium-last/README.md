# Last of Array

https://github.com/type-challenges/type-challenges/blob/main/questions/00015-medium-last/README.ja.md

<a href="https://tsch.js.org/15/play/ja" target="_blank"><img src="https://img.shields.io/badge/挑戦する-3178c6?logo=typescript&logoColor=white" alt="挑戦する"/></a>

## 例

```ts
type arr1 = ['a', 'b', 'c']
type arr2 = [3, 2, 1]

type tail1 = Last<arr1> // expected to be 'c'
type tail2 = Last<arr2> // expected to be 1
```

## 解答

```ts
type Last<T extends any[]> = T extends [...infer _, infer Last] ? Last : never;
```

<a href="https://www.typescriptlang.org/play?ssl=27&ssc=80&pln=26&pc=1#code/PQKgUABBCMCsEFoIBkCGBnALhA9gMwgEEAnY1AT0kQRtqoCNyiA7TACx2aYDEBXCABQABVKzy8AlBADEgWjlAWL4zUpCmCrSNEQFcxgeVU1UAHwRAygyA7BkBNUYBkMwOYMgewYAKuQAOAUwDKAY2IBLJ9gAsAHQADIAyDIAVxoAWmoCqDIAxDIB+DICaDPoQgLKJgOhKEAAG9lkQgEkMgOvKgIoMgGvKgFEMgIAMgLoMpoAA5oAx+qaAgZGABL6mgNHq+YAr8YmAcjaAFK6AIW6AVgzZaFgAPPYGefmA+dqAoxGA6gyAZgyA8gyABgzRgCIMgEAMKYDR8oASDIAODClZl5joVJjOLhDKxNAQALwQANoA5KhfADQQL70f6AjxfAC6t3uj1IACY3p8AMwA2EA6CQqGuCCYVDeAA2L3eE0wkye0CMwGAEBcAA9XB5MC4ACbYnAQegPL5gzEPHH4+FEjAkp6wilU2n0xkszBsjkwKiXLIpIwAcW8mAAErx6NZAF0egFioxKAaIZAFj-bEwmCc6AAXJTrh42IEAFboQI4YgAc2AcGATtQYBAwDUoAgAH1wxHIxGTMZANYMgGaGQA-DIBJhnygAwowCmimGoznQxBA2o7ljidNqTTGcwmehHlwPuCjO97GWK1XPoF295mHgXMQwwDO93e8TwRAAPwoIUQa0QZguABuPYA3MGQNnc5GIIAxhkAnQyACYZAI0Mie3a-X4fzQe8AFsnO7sEWHgBvCAAUQAjrxUHiAc+6S4GRAAF8IDwYgcEvQEhHvBAHU-PEXGYD0XHQYBeEwfF0C+QtoQ8DAkIRD4qB-SVJjfD88UmEsPmRCBURges0QMAw-kI38GRI99PwooVJg+AQpFeIxoFhain1QacsB8BDAPoiBRPEzBJI9QDGOYjEQ1PDdAEJrUxt03QBhhkAdYYT1Pc8wFAKgjEAY8jABVvfJAEdFQBIc2NM0LStW1gHtR0XTdT1vVgYBRHQAB3HtfX9QwIBs-JAGjI01zUtG07XQB1nVdd0vR9dAcDxVDvE4G4ItqQA1uQsSwXIS9zPNSnyvT9AMgyAA" target="_blank"><img src="https://img.shields.io/badge/解答-3178c6?logo=typescript&logoColor=white" alt="解答"/></a>