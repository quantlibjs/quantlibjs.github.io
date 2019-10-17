
# quantlib.js [![npm version](https://badge.fury.io/js/%40quantlib%2Fql.svg)](https://badge.fury.io/js/%40quantlib%2Fql) [![](https://data.jsdelivr.com/v1/package/npm/@quantlib/ql/badge?style=rounded)](https://www.jsdelivr.com/package/npm/@quantlib/ql) [![Twitter Follow](https://img.shields.io/twitter/follow/quantlibjs.svg?style=social&maxAge=3600)](https://twitter.com/quantlibjs)

## get started

1. open https://quantlib.js.org with morden web browser, like chrome, firefox, etc...

2. select a `spec` or `example` from navbar. `spec` source will be displayed on left panel, `spec` will be run with [jasmine](https://github.com/jasmine/jasmine) by your web browser, and test result will be displayed on right panel

## docs
* https://quantlib.js.org/docs
* offical c++ quantlib doc: https://www.quantlib.org/reference/

## install

### CDN

#### jsdelivr
* latest version: https://cdn.jsdelivr.net/npm/@quantlib/ql@latest/ql.mjs
* version `x.y.z` : https://cdn.jsdelivr.net/npm/@quantlib/ql@x.y.z/ql.mjs

#### unpkg
* latest version: https://unpkg.com/@quantlib/ql@latest/ql.mjs
* version `x.y.z` : https://unpkg.com/@quantlib/ql@x.y.z/ql.mjs

### npm
```
npm install @quantlib/ql
```

## usage

this library is still at early stage, many test cases fails, it's for enthusiast only.

A static [report](https://quantlib.js.org/test-suite/) is updated manually monthly, so you could see the overall test pass rate.

### assumption

this project assumes `user` is already familiar with the `c++` [QuantLib](https://github.com/lballabio/QuantLib)

### web browser

`ql.mjs` is [ESM format](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Modules), when using in html script tag, make sure to have script type set to "module"

```html
<script type="module">
    import {someclass} from 'https://cdn.jsdelivr.net/npm/@quantlib/ql@latest/ql.mjs'
    const obj=new someclass();
    obj.dosomething();
</script>
```

### notebook

checkout https://observablehq.com/@quantlib

### node.js
`quantlib.js` also works in `node.js` env, after installing with `npm`, pass `--experimental-modules` to `node` to use ESM javascript file

```sh
node --experimental-modules test.mjs
```

in `test.mjs`
```js
import {someclass} from '@quantlib/ql'
const obj=new someclass();
obj.dosomething();
```

### typescript
`ql.d.ts` can be found in the same location as ql.mjs

```ts
import {someclass} from '@quantlib/ql'
const obj:someclass = new someclass();
obj.dosomething();
```

## test-suite & example

repo:
* https://github.com/quantlibjs/test-suite
* https://github.com/quantlibjs/examples

converted to `javascript` from the `c++` [quantlib](https://www.quantlib.org/) [test-suite](https://github.com/lballabio/QuantLib/tree/master/test-suite) & [Examples](https://github.com/lballabio/QuantLib/tree/master/Examples)

## credit

* C++ QuantLib project: https://quantlib.org
* C++ QuantLib-noboost: https://github.com/haozhangphd/QuantLib-noBoost
* mathjs: https://mathjs.org
* js.org: https://github.com/js-org/js.org

## Support
* Follow us on Twitter: [@quantlibjs](https://twitter.com/quantlibjs)
* Facebook page: https://www.facebook.com/quantlibjs/
* Google group: https://groups.google.com/d/forum/quantlibjs/
* Group email: quantlibjs@googlegroup.com
* reddit: https://reddit/com/r/quantlibjs

## blog
* https://quantlib.js.org/blog/