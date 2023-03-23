# Pick

https://github.com/type-challenges/type-challenges/blob/main/questions/00004-easy-pick/README.ja.md

<a href="https://tsch.js.org/4/play/ja" target="_blank"><img src="https://img.shields.io/badge/挑戦する-3178c6?logo=typescript&logoColor=white" alt="挑戦する"/></a>

## 例

```ts
interface Todo {
  title: string
  description: string
  completed: boolean
}

type TodoPreview = MyPick<Todo, 'title' | 'completed'>

const todo: TodoPreview = {
  title: 'Clean room',
  completed: false,
}
```

## 解答

```ts
type MyPick<T, K extends keyof T> = {
  [P in K]: T[P]
}
```

<a href="https://www.typescriptlang.org/play?#code/PQKgUABBAsELQQAoEsDGBrS8491gRgJ4QCCAdgC4AWA9mcQGICuEAFAAICGlAZkwJQQAxIFwlQFi+wpmWR1h+JsgA2FOMjJgsQrREBXMYHlVDVEAivoH8GQD3xJwHYMgaPVAZwyAfhkBjDIGKGQFcMLgAYoMAHgAqADQQANIAfB6ASQyA-vKAFK6A2gyAWgyAgAwefh6A0gyAkQwewR6WgOsMgLcMgIsMLhGAvUaAX4qAmgyA0QzWEYD52oCjEYDqDIB+DNWAQAyGEIDR8oASDIAODIBY-70eExQAzlhqFACmAE48nKjzEH40ACY0EADeWFAUyBSK8wBcEFMUi2oA5ocQW-NTqLcADsd0l9e3ZA9QKCoGgAW3eZwWW0u+BoNDO3CwAF9ehRCO91psdohFvMAG7IeYAdwgAF4IABZQjedD+bY0IIAcmOp3mDIgAB8IAzgWCIfMtgzQr1gWRrhAKHTLpiaNi8QTiWSDoDAcyzpcGQBheFkCCLWEghkBR5A0Hg+aQy4rRRTeZGqDIqATDy9UIQADiJwAEkx8IBzBkAXR6AWKi6iMqBQKO8pudgMBpqgqAA6ABWUwTNEWd2A0GASc4YBAwA0oAgAH0y+WK+WIIBlBmrgGsGQDNDPZAJMMEUAGFGAU0VS5WeyWIAWNKj0RSqWgaYEQhB5gAPBZkLZTCDoeaEGg8DauxVYADaiAgahCAF0pbvD2BkWBi72exBHIBOhkAEwyARoZ7Hfu9eqwPkGD0xRxWj1j2CAAFEAEcmE4RQgmA6d0VQP9EQgHg9RBLl2CHeY4HjSCzn+F5gCYY5rQZQcAIgVBOBtRcyW3LAYLgigfDAiDFCY2D5ng-kAEYgkpalaR2RlVVZUJRLtED2PgpjwMgtiGP5AAmXjR18aUhJOM42U5blTT5AVRNCcSYwgdCpjgGcGPMxY9UWLA+LHAT6S5YStK5HkzUhVyGTUXFIOQfSjTPMA5iWFY1g2Ol9iwYSfhue4sGeV4Pi+MhYr+AFyN081+WhWFtXPDQQuWVZ1nojjIS4qKjg0i4rji-4CuCyhQpKiT5K2BSqvFGq0vik1eWyqEIBhOF5gRC8rw-KtAEJrSw70cQBhhnyd8pv7QtQCwV1AGPIwAVbwiQBHRUASHMQzDCMoxjONExTNMMyzYBuCmQklhzPMoG2vbAGjI2pQ3DSNo1jV4rtTdNM2zKY4UImRRU2iBAF0GSxADW5SxACaowAZDJ+s7-su5Ngdu3N80LIA" target="_blank"><img src="https://img.shields.io/badge/解答-3178c6?logo=typescript&logoColor=white" alt="解答"/></a>

