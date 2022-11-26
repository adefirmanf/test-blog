---
layout: post
author: Ade Firman Fauzi
tags: [javascript, issue]
---

0 in javascript treated as false, careful if there any code had validation something like this.

`const value = {a : 0}`

Developer want to check `undefined` value if a doesn't exist
`const isTrue = value.a ? true : false`

If expected was `true`, it will treated as `false`. Add another validation i.e

- `Object.keys(value).include(”a”)`
- `if typeof value.a === undefined`
