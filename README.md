[![Twitter Follow](https://img.shields.io/twitter/follow/quantlibjs.svg?style=social&maxAge=3600)](https://twitter.com/quantlibjs)

[![](https://data.jsdelivr.com/v1/package/npm/@quantlib/ql/badge)](https://www.jsdelivr.com/package/npm/@quantlib/ql)

# quantlib.js

## get started

#### open https://quantlib.js.org with morden web browsers, chrome, firefox, etc...

#### select a test `spec` or `example` from top menu
![snap1](/64322073-6c73a980-cff4-11e9-9433-3928631538f4.png)

`spec` source will be displayed on left panel, `spec` will be run by [jasmine](https://github.com/jasmine/jasmine) and test result will be displayed on right panel
![snap2](/64322085-73022100-cff4-11e9-8a84-305e65405621.png)

>this is a working in progress project, the lib itself, test cases and examples are not complete


## install

### CDN
https://cdn.jsdelivr.net/npm/@quantlib/ql/ql.mjs

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
    import {someclass} from '/pathto/ql.mjs'
    const obj=new someclass();
    obj.dosomething();
</script>
```

### node.js
`quantlib.js` can also be run using `node.js`, after downloading the code to your local drive:

```sh
node --experimental-modules test.mjs
```

in `test.mjs`
```js
import {someclass} from 'pathto/ql.mjs'
const obj=new someclass();
obj.dosomething();
```

### typescript
`ql.d.ts` file will be published later

## doc

the generated doc from source code is not as good as official c++ QuantLib documentation, so we might not publish docs at all, please refer to offical c++ quantlib doc: https://www.quantlib.org/reference/

## test suite

repo: https://github.com/quantlibjs/test-suite

following the `c++` [quantlib](https://www.quantlib.org/) [test-suite](https://github.com/lballabio/QuantLib/tree/master/test-suite) code, converted to js code

## example

repo: https://github.com/quantlibjs/examples

following the `c++` [quantlib](https://www.quantlib.org/) [Examples](https://github.com/lballabio/QuantLib/tree/master/Examples) code, converted to js code

## Support
* Follow us on Twitter: @quantlibjs
* Google group: https://groups.google.com/d/forum/quantlibjs
* Group email: quantlibjs@googlegroup.com
