# Chainable Options

https://github.com/type-challenges/type-challenges/blob/main/questions/00012-medium-chainable-options/README.ja.md

<a href="https://tsch.js.org/12/play/ja" target="_blank"><img src="https://img.shields.io/badge/挑戦する-3178c6?logo=typescript&logoColor=white" alt="挑戦する"/></a>

## 例

```ts
declare const config: Chainable

const result = config
  .option('foo', 123)
  .option('name', 'type-challenges')
  .option('bar', { value: 'Hello World' })
  .get()

// expect the type of result to be:
interface Result {
  foo: number
  name: string
  bar: {
    value: string
  }
}
```

## 解答

```ts
type Chainable<T = {}> = {
  option: <K extends string, V>(key: K extends keyof T ? never : K, value: V) => Chainable<Omit<T, K> & Record<K, V>>,
  get: () => T
}
```

<a href="https://www.typescriptlang.org/play?#code/PQKgUABBCMBMEFoIGEAWBDAlgO3QIwBsBTCAeQAcAXTAe2wGdJEEXWm8BPCAQW0tTpcAYgFcIACgAC6PgDMRASggBiQLRygLF8V6cuQKYAxump0wTZeYiArmMDyqqagApdADd0AZX0AnTFQiBzBkD2DICADICDDIDlDIAlDIDPDID3yoC-AYBWDIBVDIDrDIDtDIDnDJGAMgyAEQyA8gyA-vKA8QyAMQyAfgyAmgyAQAyA6gyA0gw1gQAqHORE7l4+gNYMgOBKgFEMgP9mgBIMgPoMgBYMgLIMgYDG1jV5gNHqgEkMgBtygIoMgNEMgMoMY1m+E5V1gPj-dhCbgHYMgE1RgDIZAYGJgGsMgB0MoYD1DIATDL6AQQwvgJcMgJ0MX0AqvJfQAiDCCzr5AhAAAY0Ki0bDiADWRA4ABoIC4CCIiApoRAxjCAOZESjiPEQM4QeCAEwYzoAi1MADqaLQALxoBs+Qq6yWgCztQCV-jVAGYMeUABgyAVQYQVVYfC6PjboA4OSGgEiGEojQC1DIAfhjGgBIFRYFQDGDALAH-OgAp1Kn6OiyTBEylLQCHRoBWfT2lSqgABzQBCvoAQt3igAVfQA55v5iaTZYA15UA6fqc7ZdGplGqAcIZAGIMVROgGj5IaABwYTtCs5RGFAACZEfQEdAeEjmhiUCDly1EgBcKAwOHwxBO5foldL9BEBErAF4qxarUwoAA6OHGREAclkNBok4xcAAzAphxAx9Kp7gALZEecQSeUVpEBD6DAEYjYEn0ScrqCj8cI8STvAlvcAb0x6GxRHrk4AEkQ540BAADqNAeAQeaThAAC+t53iOJJkiuTDAMAEBEAAHm0+iVvwJCHm0EA0LIECdt2eHAXgP5MDglBEB4sjoPoJAAEpEF2PYQG+q4zjQ9bYCIW7UR4q7bj+EDtl4l6ri+Hj1jxd53liOL1lJOBEquMFMNpUBZtCJznNYVyLIAx5F5CMgCBDF0EAAFb0MAOaUoAtwyPIAwwwvIsgAfZnkgCj+oAgZH+IAQgx9GUgDaDIAyQxVPMgA3DIAmwyANcMZyuR5wqrN5IJCmKEqZiiHD4gG0LqZe+JnIA-gyLIA68qrGsgTQipRAFYA33KAPCGZxLNVazrGMgB3ctygqfIA05YguFUWADAqgAaDDCeX4lk1IQIAe2qAIR2oolFsYzBaFkVJkwAB8EAAOKYJQf4iHgviAF0egCxUZygBY-6glCUOQ9C1mhOaniO9ljh4RLAHAwC2egYAgMApigBAAD6UPQzD0OnJsXSAM0M6qAJMMiyABhRgCmipDsO4xDEAg6YhEkGgWC4IQRAADxNBA-ZvjB+100wD50PWlMANIYZh9HYHm9CSZQ0lEhiABqu3Iqi9ac1hPN8xAeUkRANMAPwQNgRBOAxEBSxiDX1iLSi9vtpNNhTlOkFux3Uxi7P7QAZBA7Hmh4eYc6Lu27WiTBIfW5K0-tTRgNpYDg3juMQIAYwx-G8gCNDOqfw42HcOE5gW7kOBeFHtxPB6CiGIAKLYYWlYwRAsgeDQW77pIxMnmeF5XsAIjUAQ16mAWRYlmWdDthA6D1ib5MtmAbYdhxFHQLTfdMOuE5Pnxe5LvBs+Ps+r4Yh+ev7gBQGgeBkHQXBM8s5u6A7nuB5HnXX4NxxN4z0h5KmKPZHjz28D9kD94bk+4kXzINB8IeDVmfXc8E0IQBrvQBAWEcKUBgR4Cuolv5z0nH-DEk5iy9z-svR+KEX7kR7IuKeX81wn1-qA-+2BAGoC1jg1C6EoEwKLrhBBSDj4-zQZQhcsBlwP1JE-MAxMqzoHoBxKeABtJghc4GU24LnKmxNFaEMoNAAuLD6J5mgB7L2UAZHFzkQoymSjSIqNgOouBRA8ywB0dIjRhjMAomMUeZRb9KCLgscXKxi5bEAF0iZZ30bhKxk8mZQD4gJISIl2AlgUquLexVNJQF0iAncalBYaSDgEoiQTNEf24kwcS6ShZZKEYEjR3ip6KVSRJQSwkGKlNDknOGgBCazOH8COblkiJ2aQTUGoA9oQFMoAFW9FiAEdFQAkOZ3Qek9F6b16AfS+uBX6-0ZD0AAO4MQBqQ-aIzFiAGjI9Y91HrPVeo5BZqBPr0G+is2AwB6A0GxBOXMEB9qAF0GM4gA1uUuFcY5syznvUuUsn62zgagyAA" target="_blank"><img src="https://img.shields.io/badge/解答-3178c6?logo=typescript&logoColor=white" alt="解答"/></a>