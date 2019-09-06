# quantlib.js

## get started

#### use modern web browser to open https://quantlib.js.org

#### select a test `spec` or `example` from top menu
![snap1](/64322073-6c73a980-cff4-11e9-9433-3928631538f4.png)

`spec` source will be displayed on left panel, `spec` will be run by [jasmine](https://github.com/jasmine/jasmine) and test result will be displayed on right panel
![snap2](/64322085-73022100-cff4-11e9-8a84-305e65405621.png)

>this is a working in progress project, the lib itself, test cases and examples are not complete


## Installation
code is not in npm or other package repo, as this is a on going project, code is located at https://quantlib.js.org/ql.mjs

for now it's recommended to test using quantlib.js.org website

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

## test suite

repo: https://github.com/quantlibjs/test-suite

following the `c++` [quantlib](https://www.quantlib.org/)[test-suite](https://github.com/lballabio/QuantLib/tree/master/test-suite) code, converted to js code

## example

repo: https://github.com/quantlibjs/examples

following the `c++` [quantlib](https://www.quantlib.org/) [Examples](https://github.com/lballabio/QuantLib/tree/master/Examples) code, converted to js code

## Support
* Follow us on Twitter: @quantlibjs
* Email: quantlib.js@outlook.com
