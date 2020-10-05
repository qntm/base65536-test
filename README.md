# base65536-test

These are language-agnostic test case files for the Base65536 encoding. For more about this encoding, see the JavaScript implementation, [`base65536`](https://github.com/qntm/base65536).

This repository contains raw data files only. In order to validate your Base65536 implementation against them, you will probably need to create an adapter which can consume them. For example, `base65536` has an adapter written in TypeScript, [using Jasmine](https://github.com/qntm/base65536/blob/6ea6b4b5fa0f475439a1a98162701561047479fd/src/test/base65536.spec.ts).

## Structure

### `data/pairs`

Each binary file e.g. `demo.bin` has a UTF-8 text counterpart e.g. `demo.txt`. A correct Base65536 implementation encodes the binary to the text and decodes the text to the binary. These comparisons should be bit-for-bit accurate. Note the absence of line endings in the text.

### `data/bad`

A correct Base65536 implementation should fail to decode these text files.

## Installation

```shell
npm install base65536-test
```
