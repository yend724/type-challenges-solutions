# Tuple to Object

https://github.com/type-challenges/type-challenges/blob/main/questions/00011-easy-tuple-to-object/README.ja.md

<a href="https://tsch.js.org/11/play/ja" target="_blank"><img src="https://img.shields.io/badge/挑戦する-3178c6?logo=typescript&logoColor=white" alt="挑戦する"/></a>

## 例

```ts
const tuple = ['tesla', 'model 3', 'model X', 'model Y'] as const

type result = TupleToObject<typeof tuple> // expected { 'tesla': 'tesla', 'model 3': 'model 3', 'model X': 'model X', 'model Y': 'model Y'}
```

## 解答

```ts
type TupleToObject<T extends readonly any[]> = {
  [K in T[number]]: K
}
```

<a href="https://www.typescriptlang.org/play?#code/PQKgUABBCM0QtBAKgVwA4BsCmEAuB7CAeQCMArLAY10gXnodpIE8IBnASwDt98uIAFAAFOPPgEoIAYkC4SoCxfafnJVc8ANZZmbMLSl6IgK5jA8qo6ogfoZA6wyBrhkBJDIHXlQIoMgNeVAUQyBABkC6DIDsGQCAqgEgUvDWZgADcAQwwULBtAQGNAEwZAKoZANYZADoZAcoZAeoZACYYvQGj1QGsGQEhNQG3jQE0GQGiGXJtAfO1AUYjAdQZAPwZSwCAGUwhAaPlACQZABwZALH-2gANh3G0oSj42XDx0bAgAXggAbQByXCw2DDCVgBoIFYBbfAATLAwIAGZd-aPT84ANa8OTs4gATRWAXQgwtggJrhTdq4ZhoHAAJw2KAw00WqEwWCQ+FIFGoAB4QWD8AAzGYIgB8EGAwAgWAAHmDqFhjhAAN54DZbABc+3Wm22e2ed0uKxZXNeV05t1ejz5woeT3F715Nxe5w+AF9aMNBu1CQBxDi4AASKBIgHMGQBdHoBYqIqfQAFrhcGg2EziaNKOaAHRkNhO-DggDmwFgwDIYTAIGAOlAEAA+hHI1HIxBAMoMsfygGaGQA-DIBJhhsgAwowCmiuHo3mwxAgzpMTh4dgkSiVGikKSyesuMc-pCwsc+BhWGEuMwlp9CYtabQlgBpCDcZBLLgoA4kLDgz6fFlDsBKsCh-N5iCAMYZAJ0MWUAjQzJ7e59cxoscA5oD3TEt0iAAUQAjigIns7xSVBAFRBseD8Ad9kIJbwI6ETYFwnobMAKC4BwGBsCsOgAlMeJzIsqxslskpyjyQrYY8uHch83y-P8kw0Eh16zFgAByU4zuCCzLNAewAEx7BcewACzEX8FFgBRKFYAAshwZKMUszH7Cx1wcfsnFfD8vFkcWoI4JQvwbOJtBvpSuBoo+z4YNWVEVso6Iljign4ns9IYWEfJ2SsADcsrclcYrYVcLn8hKHnco83lSh8fmvB8n74tZ2nvuiBkRMZCKmaiekWbiuBUbR06ztZt7QCy0AuSxLIsS5FwshcLmcSynHhZFUA6VWsVGWWiLImZyWqZZaUIiJZLZfSuUwN50l8tJJVld58l8vJNU7GAnwhiAx4ngWgCE1l426boAwwwWEtJ6FsGoC0ISgDHkYAKt42IAjoqAJDmZqWtatr2mwjoum6Hrer6nZsAA7rOfoBlAJ3nYA0ZHlBaVo2nawAOs6rrul6PrQMAbD4JEMGTEdEDeIAa3JeIATVGADIZYP3ZD0MvXD3r+oGwZAA" target="_blank"><img src="https://img.shields.io/badge/解答-3178c6?logo=typescript&logoColor=white" alt="解答"/></a>

