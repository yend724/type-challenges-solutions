# Pop

https://github.com/type-challenges/type-challenges/blob/main/questions/00016-medium-pop/README.ja.md

<a href="https://tsch.js.org/16/play/ja" target="_blank"><img src="https://img.shields.io/badge/挑戦する-3178c6?logo=typescript&logoColor=white" alt="挑戦する"/></a>

## 例

```ts
type arr1 = ['a', 'b', 'c', 'd']
type arr2 = [3, 2, 1]

type re1 = Pop<arr1> // expected to be ['a', 'b', 'c']
type re2 = Pop<arr2> // expected to be [3, 2]
```

## 解答

```ts
type Pop<T extends any[]> = T extends [...infer First, infer _] ? First : [];
```

<a href="https://www.typescriptlang.org/play?ssl=29&ssc=78&pln=29&pc=1#code/PQKgUABBCMBsEFoIAUD2AHSiE91gRgJ4QCCAdgC4AWqZxAYgK4QAUAAgIaUBmjAlBADEgWjlAWL5COAJ0kdCYLIMURAVzGB5VXlQAfBEDKDIDsGQE1RgGQzA5gyB7BgAqhdAFMAygGNJAS3QUIAFgB0ABkAyDIAVxoAWmoCqDIAxDIB+DICaDBoQgLKJgOhKEAAGFskQgEkMgOvKgIoMgGvKgFEMgIAMgADmgDH6eoCBkYAEvhmAJmmAIgyA+gyJGYAr8VGAcjaAFK6AIW6AVgwpaOgAPBaa6RmA+dqAoxGA6gyAZgyA8gyABgwhDYBADLGA0fKAEgyADgyxyccUAM5YFNY2EFKS0BAAvBAA2gDkHK8ANBCv+F8-Dn+rwAJq8ALoXK43aQAJkeLwAzN8Yd9oBDIbYIJIbPcnsMRrdoNpgMAIDYAB62BwUGzAiAUVAQfDXN4fb6-IGAiFQS6Y7FwvEYAmw4mkilUml0hlMllIiAw7kpY6xEAgQBSDBEcqqAFwQQAwKoANy0A1gwpOxUZzcCjJIpDRinKjWlIAVTI9otVoggCCGWYmQCyDNFANIMgHx-2LaADizgoAAlGPgTIAuj0AsVFRQDRDIAsf6oFAo6FO2pJZwcVC8ACtTl5UJIAObAODAYscMAgYDyUAQAD6Hc7Xc7uh0RsAzQyAH4ZAJMMGUAGFGAU0V292Z22IE35LzrviLGTyTSyMDTjc6M8wdonquKRuty8vOfnGRuDZJBB6M5JKcKN9L9fb22wRAAPx3h9PiC6nuADcLYgNOs5dhAgBjDIAnQyABMMgCNDIOMHgRBHbzs2zgALboBW7hLhAADeEAAKIAI6MBwAA23wkZSNjUhAAC+EDcJIqBYT8bBLgghbUVRNhkJWNinMAjAUM4VGnK8i5Qg4HCnCJ8LPFgdESiM5GUVRIz4s8coojA+7fHpyL7ponyqfR1IaRR1E6UKrJAn87KAuyoJGS87xOZy4KaOZlnqZpdm6R5e5+RZ6KtmhkGAITWegwVBgDDDIA6wyoWhGFgKAWDaIAx5GACreGSAI6KgCQ5qmGZZjmebAAWRaluWVY1rAwBcKcADuN51g2WgQPlGSANGR6aZtmub5qchYlmWFbVrWpyoFR4nOLQ5zdYAugx6IAa3KGEY5XDVVNUTfV1b1o2zZAA" target="_blank"><img src="https://img.shields.io/badge/解答-3178c6?logo=typescript&logoColor=white" alt="解答"/></a>