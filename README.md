
# quantlib.js [![](https://data.jsdelivr.com/v1/package/npm/@quantlib/ql/badge)](https://www.jsdelivr.com/package/npm/@quantlib/ql) [![Twitter Follow](https://img.shields.io/twitter/follow/quantlibjs.svg?style=social&maxAge=3600)](https://twitter.com/quantlibjs)

## get started

#### open https://quantlib.js.org with morden web browsers, chrome, firefox, etc...

#### select a test `spec` or `example` from top menu
![snap1](/64322073-6c73a980-cff4-11e9-9433-3928631538f4.png)

`spec` source will be displayed on left panel, `spec` will be run by [jasmine](https://github.com/jasmine/jasmine) and test result will be displayed on right panel
![snap2](/64322085-73022100-cff4-11e9-8a84-305e65405621.png)

>this is a working in progress project, the lib itself, test cases and examples are not complete


## install

### CDN

#### jsdlivr
* latest version: https://cdn.jsdelivr.net/npm/@quantlib/ql@latest/ql.mjs
* specific version: https://cdn.jsdelivr.net/npm/@quantlib/ql@x.y.z/ql.mjs

#### unpkg
* latest version: https://unpkg.com/@quantlib/ql@latest/ql.mjs
* specific version: https://unpkg.com/@quantlib/ql@x.y.z/ql.mjs

### npm
```
npm install @quantlib/ql
```

## usage

this library is still at early stage, many test cases fails, it's for enthusiast only.

### assumption

* this project assumes `user` is already familiar with the `c++` [QuantLib](https://github.com/lballabio/QuantLib)

* as `typescript`/`javascript` and `c++` are completely different languages, it's very difficult to explain all the details. for now, please refer to [test-suite](https://github.com/quantlibjs/test-suite), and [examples](https://github.com/quantlibjs/examples) code

### web browser

```html
<script type="module">
    import {someclass} from 'https://cdn.jsdelivr.net/npm/@quantlib/ql/ql.mjs'
    const obj=new someclass();
    obj.dosomething();
</script>
```

### notebook

checkout https://observablehq.com/@quantlib

### node.js
`quantlib.js` can also be run using `node.js`, after downloading the code to your local drive:

```sh
node --experimental-modules test.mjs
```

in `test.mjs`
```js
import {someclass} from '@quantlib/ql/ql.mjs'
const obj=new someclass();
obj.dosomething();
```

### typescript
`ql.d.ts` file will be published later

## doc

the generated doc from source code is not as good as official c++ QuantLib documentation, so I may not publish docs at all, please refer to offical c++ quantlib doc: https://www.quantlib.org/reference/

## test-suite & example

code repo: 
* https://github.com/quantlibjs/test-suite
* https://github.com/quantlibjs/examples

following the `c++` [quantlib](https://www.quantlib.org/) [test-suite](https://github.com/lballabio/QuantLib/tree/master/test-suite) & [Examples](https://github.com/lballabio/QuantLib/tree/master/Examples) code, converted to js code

## Support
* Follow us on Twitter: @quantlibjs
* Facebook page: https://www.facebook.com/quantlibjs/
* Google group: https://groups.google.com/d/forum/quantlibjs/
* Group email: quantlibjs@googlegroup.com
* reddit: https://reddit/com/r/quantlibjs
