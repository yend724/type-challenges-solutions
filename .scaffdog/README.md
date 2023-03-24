---
name: 'README'
root: '.'
output: '.'
ignore: []
questions:
  value: 'Please enter any text.'
---

# `{{ inputs.value }}/README.md`

```markdown
# Title

https://github.com/type-challenges/type-challenges/blob/main/questions/{{ inputs.value }}/README.ja.md

<a href="https://tsch.js.org/{{ replace(inputs.value, "-.+", "") | replace "0+" "" }}/play/ja" target="_blank"><img src="https://img.shields.io/badge/挑戦する-3178c6?logo=typescript&logoColor=white" alt="挑戦する"/></a>

## 例

{{"```ts"}}
{{"```"}}

## 解答

{{"```ts"}}
{{"```"}}

<a href="" target="_blank"><img src="https://img.shields.io/badge/解答-3178c6?logo=typescript&logoColor=white" alt="解答"/></a>
```