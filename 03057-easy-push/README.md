# Push

https://github.com/type-challenges/type-challenges/blob/main/questions/03057-easy-push/README.ja.md

<a href="https://tsch.js.org/3057/play/ja" target="_blank"><img src="https://img.shields.io/badge/挑戦する-3178c6?logo=typescript&logoColor=white" alt="挑戦する"/></a>

## 例

```ts
type Result = Push<[1, 2], '3'> // [1, 2, '3']
```

## 解答

```ts
type Push<T extends unknown[], U> = [...T, U];
```

<a href="https://www.typescriptlang.org/play?ssl=21&ssc=47&pln=21&pc=1#code/PQKgUABBDMAMCsB2CBaCAFArgZwBaVRSOIICMBPCAKwEsBDAOwHM9GIAKAAVsZd0YC2AUwAudAJQQAxIFwlQFi+0ugCcldcmAJStEQFcxgeVUNUAAYmAgirUA6AA45cJo4DsGQB0MgcoZAswyArhkDDDIHqGQAsMgD8MzoDnDIDPDIBJDID52oCjEYDqDIB+DICaDIBADIYQgNHygBIMgA4MgFj-6Q4i5NZC2ADGSjTWIgTFpRAASmWYADYiEAC8GHYAPADaAIwANBAATAC6owDk0NMAfBDAwBBDo2MzcxMEDumLAOI0IgASmKSA5gyAXR6AsVFJgNEMebgiItbYAFzLIhW4llTYlgB7JRMYBwJDAKh0MAgYAaUAQAD6SORKOREEAygzowDWDIBmhkCgEmGCKADCjAKaKiNRFIREBhGnqQh6eF6ABUIEIAB4iIQMAAm2AgmAYAGsGACAO4MfpTCAAVUW3X6lkVTNG0omAG44SByZSURBAGMMgE6GQATDIBGhkCBu1OqR1NhNAE1iBHTpEAA3hAAKIAR0wdFao3dbNK5Q6AF8IAAzJQAgQQaacOkocr8VqtLlMMrATAiGitbDTWklenlOjYMpdVYEANBkS9L0+1q9LCMyWjQbzUZDCbzduVwNCYO172+xt9NbjKWzBYdkbjTbTLs9qBV-s1uvDpu4AbTQbTdZzqWkAEA1OMdurbe72exuajQ-HoSMBfDMDbMDwq26wCE1o4DXrvIB1hktK0bTfcAoEWQBjyMAFW8IkAR0VAEhze5HmeV4PmAL4k1+f4gRBMFEGARhsFFIQlAhKFwIgaCIkAaMiHieF53k+b4sMBYFQQQfDsGPLMaABBhsAIRZAF0GRxADW5RxACaowAZDOQhi0Iwn4-lYkFIWhWEgA" target="_blank"><img src="https://img.shields.io/badge/解答-3178c6?logo=typescript&logoColor=white" alt="解答"/></a>