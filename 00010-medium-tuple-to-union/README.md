# Tuple to Union

https://github.com/type-challenges/type-challenges/blob/main/questions/00010-medium-tuple-to-union/README.ja.md

<a href="https://tsch.js.org/10/play/ja" target="_blank"><img src="https://img.shields.io/badge/挑戦する-3178c6?logo=typescript&logoColor=white" alt="挑戦する"/></a>

## 例

```ts
type Arr = ['1', '2', '3']

type Test = TupleToUnion<Arr> // expected to be '1' | '2' | '3'
```

## 解答

```ts
type TupleToUnion<T extends unknown[]> = T[number];
```

<a href="https://www.typescriptlang.org/play?ssl=23&ssc=52&pln=23&pc=1#code/PQKgUABBCMAMEFoIBUCuAHANgUwgFwHsIBVAOwEsDTJEE76aAjATwgEFS8ALK1gMVQQAFAAEAhpwBmqAJQQAxIFo5QFi+C8qUnYATgrwYcC1BSpga88xEBXMYHlVU1ED9DIHWGQNcMgOwZAJAqBpBkCRDIDOGQNMMgFUMgM8MgNHqgEkMgPiugAhGgJoMgNEMAAZoWNjIBGSUpAA8yAB8ieGA+dqAoxGA6gyAfgyxgEAMdhCA0fKAEgyADgx1ie14AM40eMzouGxaOgC8EADaAOTQEwA0EBMATLPzAMwTALp1vf0o2J14EKMpOOmZVNmDWnkQwMAQ2AAe-QDGeNgAJvhEjLhTExAAH3mS0BqwmNHaiTq1wA4uQ8AAJVCMQDmDIAuj0AsVEJQBY-1w8Hh0J0AFy3LrPLgAOgAVp0KQQtABzYBwYBUsRgEDAUygCAAfX5AsFAoggGUGEWAawZAM0MgB+GQCTDOFABhRgFNFPlCtW8iCc0zbXDHNIZYw5ZD3B5vUjvToQIwAa1IBAA7qQxutrkcxqRUABbH5adYAbm5IFV6sFEEAYwyAToZABMMgEaGaUR4Mh-marnkT3oekHHUQADeEAAogBHVBiTBzfNPbCvCAAXwgki0BE98xEOoQ5NLOFIDL2wFQeHImE64LA2eeYk6e0O4xoFZeeGyRZLmFy+n1ZxyY2gCxWcwmABYAKwANmWeC0qGwLrm25WoIPJ-+QPPl7yeRms8rr0XxdLq9SpyGtkW47teMA7m+H6bGAPJJqGgCE1q4EZhoAwwyOImSYpjB4BQNcgDHkYAKt7hIAjoqAJDmOJ4gSxKkp05LUrS9JMiyEidPa2isuyuEQIR4SANGR8S4vihIksAZKUjSdKMsysDAJ0BCYP2WTdFxgC6DK4gBrcq4gBNUYAMhmCVRIlifRklMmyHJckAA" target="_blank"><img src="https://img.shields.io/badge/解答-3178c6?logo=typescript&logoColor=white" alt="解答"/></a>