# <a href="http://kefirjs.github.io/kefir/"><img src="http://kefirjs.github.io/kefir/Kefir-with-bg.svg" width="60" height="60"></a> Kefir

Kefir — это библиотека реактивного программирования для JavaScript вдохновлено
[Bacon.js](https://github.com/baconjs/bacon.js) и
[RxJS](https://github.com/Reactive-Extensions/RxJS) с фокусом на высокую
производительность и низкое потребление памяти.

Документация [kefirjs.github.io/kefir](http://kefirjs.github.io/kefir). См.
также
[устаревшее API docs](https://github.com/kefirjs/kefir/blob/master/deprecated-api-docs.md).

[![GitHub license](https://img.shields.io/badge/license-MIT-blue.svg)](https://github.com/kefirjs/kefir/blob/master/LICENSE.txt)
[![npm version](https://img.shields.io/npm/v/kefir.svg?style=flat)](https://www.npmjs.com/package/kefir)
[![Build Status](https://travis-ci.org/kefirjs/kefir.svg?branch=master)](https://travis-ci.org/kefirjs/kefir)
[![Gitter](https://badges.gitter.im/Join%20Chat.svg)](https://gitter.im/pozadi/kefir?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge)

# Установка

Kefir available as NPM and Bower packages, as well as simple files download.

### NPM

```sh
npm install kefir
```

### Bower

```sh
bower install kefir
```

### Загрузка

See [downloads](https://kefirjs.github.io/kefir/#downloads) section in the docs.

Also available on [jsDelivr](http://www.jsdelivr.com/#!kefir).

# Поддержка браузерами

Мы не поддерживаем IE8 и ниже, а в остальном Kefir должен работать в любом
браузере.

## [Flow](https://flowtype.org/)

The NPM package ships with Flow definitions. So you can do something like this
if you use Flow:

```js
// @flow

import Kefir from "kefir";

function foo(numberStream: Kefir.Observable<number>) {
  numberStream.onValue((x) => {
    // Flow knows x is a number here
  });
}

const s = Kefir.constant(5);
// Flow can automatically infer the type of values in the stream and determine
// that `s` is of type Kefir.Observable<number> here.
foo(s);
```

# Разработка

```sh
npm run prettify    # делает исходный код красивым (запускайте это прежде чем PR будет merged)
npm run build-js    # собирает js сборщики
npm run test        # запускает все проверки
npm run test-only   # запускает только unit тесты
npm run test-debug  # runs tests with a chrome inspector connected to the node process
npm run build-docs  # собирает html файл документации
```
