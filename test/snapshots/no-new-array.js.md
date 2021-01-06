# Snapshot report for `test/no-new-array.js`

The actual snapshot is saved in `no-new-array.js.snap`.

Generated by [AVA](https://avajs.dev).

## no-new-array - #1

> Snapshot 1

    `␊
    Input:␊
      1 | const array = new Array(1)␊
    ␊
    Output:␊
      1 | const array = Array.from({length: 1})␊
    ␊
    Error 1/1:␊
    > 1 | const array = new Array(1)␊
        |               ^^^^^^^^^^^^ Do not use `new Array()`.␊
    `

## no-new-array - #2

> Snapshot 1

    `␊
    Input:␊
      1 | const zero = 0;␊
      2 | const array = new Array(zero);␊
    ␊
    Output:␊
      1 | const zero = 0;␊
      2 | const array = Array.from({length: zero});␊
    ␊
    Error 1/1:␊
      1 | const zero = 0;␊
    > 2 | const array = new Array(zero);␊
        |               ^^^^^^^^^^^^^^^ Do not use `new Array()`.␊
    `

## no-new-array - #3

> Snapshot 1

    `␊
    Input:␊
      1 | const length = 1;␊
      2 | const array = new Array(length);␊
    ␊
    Output:␊
      1 | const length = 1;␊
      2 | const array = Array.from({length});␊
    ␊
    Error 1/1:␊
      1 | const length = 1;␊
    > 2 | const array = new Array(length);␊
        |               ^^^^^^^^^^^^^^^^^ Do not use `new Array()`.␊
    `

## no-new-array - #4

> Snapshot 1

    `␊
    Input:␊
      1 | const array = new Array(1.5)␊
    ␊
    Output:␊
      1 | const array = Array.from({length: 1.5})␊
    ␊
    Error 1/1:␊
    > 1 | const array = new Array(1.5)␊
        |               ^^^^^^^^^^^^^^ Do not use `new Array()`.␊
    `

## no-new-array - #5

> Snapshot 1

    `␊
    Input:␊
      1 | const array = new Array(Number("1"))␊
    ␊
    Output:␊
      1 | const array = Array.from({length: Number("1")})␊
    ␊
    Error 1/1:␊
    > 1 | const array = new Array(Number("1"))␊
        |               ^^^^^^^^^^^^^^^^^^^^^^ Do not use `new Array()`.␊
    `

## no-new-array - #6

> Snapshot 1

    `␊
    Input:␊
      1 | const array = new Array("1")␊
    ␊
    Output:␊
      1 | const array = ["1"]␊
    ␊
    Error 1/1:␊
    > 1 | const array = new Array("1")␊
        |               ^^^^^^^^^^^^^^ Do not use `new Array()`.␊
    `

## no-new-array - #7

> Snapshot 1

    `␊
    Input:␊
      1 | const array = new Array(null)␊
    ␊
    Output:␊
      1 | const array = [null]␊
    ␊
    Error 1/1:␊
    > 1 | const array = new Array(null)␊
        |               ^^^^^^^^^^^^^^^ Do not use `new Array()`.␊
    `

## no-new-array - #8

> Snapshot 1

    `␊
    Input:␊
      1 | const array = new Array(("1"))␊
    ␊
    Output:␊
      1 | const array = [("1")]␊
    ␊
    Error 1/1:␊
    > 1 | const array = new Array(("1"))␊
        |               ^^^^^^^^^^^^^^^^ Do not use `new Array()`.␊
    `

## no-new-array - #9

> Snapshot 1

    `␊
    Input:␊
      1 | const array = new Array((0, 1))␊
    ␊
    Output:␊
      1 | const array = Array.from({length: (0, 1)})␊
    ␊
    Error 1/1:␊
    > 1 | const array = new Array((0, 1))␊
        |               ^^^^^^^^^^^^^^^^^ Do not use `new Array()`.␊
    `

## no-new-array - #10

> Snapshot 1

    `␊
    Input:␊
      1 | const foo = []␊
      2 | new Array("bar").forEach(baz)␊
    ␊
    Output:␊
      1 | const foo = []␊
      2 | ;["bar"].forEach(baz)␊
    ␊
    Error 1/1:␊
      1 | const foo = []␊
    > 2 | new Array("bar").forEach(baz)␊
        | ^^^^^^^^^^^^^^^^ Do not use `new Array()`.␊
    `