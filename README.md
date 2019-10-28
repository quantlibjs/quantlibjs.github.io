
# quantlib.js [![npm version](https://badge.fury.io/js/%40quantlib%2Fql.svg)](https://badge.fury.io/js/%40quantlib%2Fql) [![](https://data.jsdelivr.com/v1/package/npm/@quantlib/ql/badge?style=rounded)](https://www.jsdelivr.com/package/npm/@quantlib/ql) [![Twitter Follow](https://img.shields.io/twitter/follow/quantlibjs.svg?style=social&maxAge=3600)](https://twitter.com/quantlibjs)

## get started

1. open https://quantlib.js.org with morden web browser, like chrome, firefox, etc...

2. select a `spec` or `example` from menu. `spec` source will be displayed on left panel, `spec` will be run with [jasmine](https://github.com/jasmine/jasmine) by your web browser, and test result will be displayed on right panel

# Table of Contents
1. [get started](#get-started)
2. [api document](#docs)
3. [how to use](#usage)
4. [test suite & example](#test-suite--example)
5. [credit](#credit)
6. [test report](#test-report)
7. [release note](#release-note)

## docs
* https://quantlib.js.org/docs
* official c++ quantlib doc: https://www.quantlib.org/reference/

## usage

this library is still at early stage, many test cases fails, it's for enthusiast only.

A static [report](https://quantlib.js.org/test-suite/) is updated manually monthly, so you could see the overall test pass rate.

### assumption

this project assumes `user` is already familiar with the `c++` [QuantLib](https://github.com/lballabio/QuantLib)

### install

#### CDN

##### jsdelivr
* latest version: https://cdn.jsdelivr.net/npm/@quantlib/ql@latest/ql.mjs
* version `x.y.z` : https://cdn.jsdelivr.net/npm/@quantlib/ql@x.y.z/ql.mjs

##### unpkg
* latest version: https://unpkg.com/@quantlib/ql@latest/ql.mjs
* version `x.y.z` : https://unpkg.com/@quantlib/ql@x.y.z/ql.mjs

#### npm

official registry:

```
npm install @quantlib/ql
```

github registry:

```
npm install @quantlibjs/ql
```

#### web browser

`ql.mjs` is [ESM format](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Modules), when using in html script tag, make sure to have script type set to "module"

```html
<script type="module">
    import {someclass} from 'https://cdn.jsdelivr.net/npm/@quantlib/ql@latest/ql.mjs'
    const obj=new someclass();
    obj.dosomething();
</script>
```

#### node.js
`quantlib.js` works in `node.js` env, after installing with `npm`, pass `--experimental-modules` to `node` to use ESM javascript file

```sh
node --experimental-modules test.mjs
```

in `test.mjs`
```js
import {someclass} from '@quantlib/ql'
const obj=new someclass();
obj.dosomething();
```

#### typescript
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

these are the code loaded and executed in https://quantlib.js.org

## credit

* C++ QuantLib project: https://quantlib.org
* C++ QuantLib-noboost: https://github.com/haozhangphd/QuantLib-noBoost
* mathjs: https://mathjs.org
* phosphor: https://github.com/phosphorjs/phosphor
* js.org: https://github.com/js-org/js.org

## link
* Google group: https://groups.google.com/d/forum/quantlibjs/
* Follow us on Twitter: [@quantlibjs](https://twitter.com/quantlibjs)
* Facebook page: https://www.facebook.com/quantlibjs/
* blog: https://quantlib.js.org/blog/
* notebook: https://observablehq.com/@quantlib

## test report
v0.2.3 total: 274, passed: 269, failed: 5, pending: 0

Exchange-rate tests
- [x] Testing direct exchange rates...
- [x] Testing derived exchange rates...
- [x] Testing lookup of direct exchange rates...
- [x] Testing lookup of triangulated exchange rates...
- [x] Testing lookup of derived exchange rates...
Money tests
- [x] Testing money arithmetic without conversions...
- [ ] Testing money arithmetic with conversion to base currency...
- [ ] Testing money arithmetic with automated conversion...
Business day convention tests
- [x] Testing business day conventions...
Calendar tests
- [x] Testing calendar modification...
- [x] Testing joint calendars...
- [x] Testing US settlement holiday list...
- [x] Testing US government bond market holiday list...
- [x] Testing New York Stock Exchange holiday list...
- [x] Testing TARGET holiday list...
- [x] Testing Frankfurt Stock Exchange holiday list...
- [x] Testing Eurex holiday list...
- [x] Testing Xetra holiday list...
- [x] Testing UK settlement holiday list...
- [x] Testing London Stock Exchange holiday list...
- [x] Testing London Metals Exchange holiday list...
- [x] Testing Milan Stock Exchange holiday list...
- [x] Testing Russia holiday list...
- [x] Testing Brazil holiday list...
- [x] Testing South-Korean settlement holiday list...
- [x] Testing Korea Stock Exchange holiday list...
- [x] Testing China Shanghai Stock Exchange holiday list...
- [x] Testing China Inter Bank working weekends list...
- [x] Testing end-of-month calculation...
- [x] Testing calculation of business days between dates...
- [x] Testing bespoke calendars...
Date tests
- [x] Testing ECB dates...
- [x] Testing IMM dates...
- [x] Testing ASX dates...
- [x] Testing dates...
- [x] Testing ISO dates...
- [x] Testing parsing of dates...
- [x] Testing intraday information of dates...
Day counter tests
- [x] Testing actual/actual day counters...
- [x] Testing actual/actual day counter with schedule...
- [x] Testing simple day counter...
- [x] Testing 1/1 day counter...
- [x] Testing business/252 day counter...
- [x] Testing thirty/360 day counter (Bond Basis)...
- [x] Testing thirty/360 day counter (Eurobond Basis)...
- [x] Testing intraday behavior of day counter ...
Period tests
- [x] Testing period algebra on years/months...
- [x] Testing period algebra on weeks/days...
- [x] Testing period parsing...
Schedule tests
- [x] Testing schedule with daily frequency...
- [x] Testing end date for schedule with end-of-month adjustment...
- [x] Testing that no dates are past the end date with EOM adjustment...
- [x] Testing that next-to-last date same as end date is removed...
- [x] Testing that the last date is not adjusted for EOM when termination date convention is unadjusted...
- [x] Testing that the first date is not duplicated due to EOM convention when going backwards...
- [x] Testing CDS2015 semi-annual rolling convention...
- [x] Testing the constructor taking a vector of dates and possibly additional meta information...
- [x] Testing that a four-weeks tenor works...
Timegrid tests
- [x] Testing TimeGrid constructor with additional steps...
- [x] Testing TimeGrid constructor with only mandatory points...
- [x] Testing TimeGrid construction with n evenly spaced points...
- [x] Testing if the constructor raises an error for empty iterators...
- [x] Testing if the constructor raises an error for negative time values...
- [x] Testing returned index is closest to the requested time...
- [x] Testing returned time matches to the requested index...
- [x] Testing mandatory times are recalled correctly...
array tests
- [x] Testing array construction...
- [x] Testing array functions...
auto-covariance tests
- [x] Testing convolutions...
- [x] Testing auto-covariances...
- [x] Testing auto-correlations...
Covariance and correlation tests
- [x] Testing matrix rank reduction salvaging algorithms...
- [x] Testing positive semi-definiteness salvaging algorithms...
- [x] Testing covariance and correlation calculations...
Credit risk plus tests
- [x] Testing extended credit risk plus model against reference values...
fast fourier transform tests
- [x] Testing complex direct FFT...
- [x] Testing convolution via inverse FFT...
Integration tests
- [x] Testing segment integration...
- [x] Testing trapezoid integration...
- [x] Testing mid-point trapezoid integration...
- [x] Testing Simpson integration...
- [x] Testing adaptive Gauss-Kronrod integration...
- [x] Testing adaptive Gauss-Lobatto integration...
- [x] Testing non-adaptive Gauss-Kronrod integration...
- [x] Testing two dimensional adaptive Gauss-Lobatto integration...
- [x] Testing Folin's integral formulae...
- [x] Testing discrete integral formulae...
- [x] Testing discrete integrator formulae...
- [x] Testing piecewise integral...
Low-discrepancy sequence tests
- [x] Testing random-seed generator...
- [x] Testing 21200 primitive polynomials modulo two...
- [x] Testing randomized low-discrepancy sequences up to dimension 21200...
- [x] Testing randomized lattice sequences...
- [x] Testing Sobol sequences up to dimension 21200...
- [x] Testing Faure sequences...
- [x] Testing Halton sequences...
- [x] Testing Mersenne-twister discrepancy...
- [x] Testing plain Halton discrepancy...
- [x] Testing random-start Halton discrepancy...
- [x] Testing random-shift Halton discrepancy...
- [x] Testing random-start, random-shift Halton discrepancy...
- [x] Testing Jaeckel-Sobol discrepancy...
- [x] Testing Levitan-Sobol discrepancy...
- [x] Testing Levitan-Lemieux-Sobol discrepancy...
- [x] Testing unit Sobol discrepancy...
- [x] Testing Sobol sequence skipping...
Matrix tests
- [x] Testing eigenvalues and eigenvectors calculation...
- [x] Testing matricial square root...
- [x] Testing Higham matricial square root...
- [x] Testing singular value decomposition...
- [x] Testing QR decomposition...
- [x] Testing QR solve...
- [x] Testing LU inverse calculation...
- [x] Testing LU determinant calculation...
- [x] Testing orthogonal projections...
- [x] Testing Cholesky Decomposition...
- [x] Testing Moore-Penrose inverse...
- [x] Testing iterative solvers...
Mersenne twister tests
- [x] Testing Mersenne twister...
NumericalDifferentiation tests
- [x] Testing numerical differentiation using the central scheme...
- [x] Testing numerical differentiation using the backward scheme...
- [x] Testing numerical differentiation using the Forward scheme...
- [x] Testing numerical differentiation of first order using an irregular scheme...
- [x] Testing numerical differentiation of second order using an irregular scheme...
- [x] Testing numerical differentiation of sin function...
- [x] Testing coefficients from numerical differentiation by comparison with results from Vandermonde matrix inversion...
ode tests
- [x] Testing adaptive Runge Kutta...
- [x] Testing matrix exponential based on ode...
- [x] Testing matrix exponential of a zero matrix based on ode...
Optimizers tests
- [x] Testing optimizers...
- [x] Testing nested optimizations...
- [x] Testing differential evolution...
RNG traits tests
- [x] Testing Gaussian pseudo-random number generation...
- [x] Testing Poisson pseudo-random number generation...
- [x] Testing custom Poisson pseudo-random number generation...
Rounding tests
- [x] Testing closest decimal rounding...
- [x] Testing upward decimal rounding...
- [x] Testing downward decimal rounding...
- [x] Testing floor decimal rounding...
- [x] Testing ceiling decimal rounding...
sampled curve tests
- [x] Testing sampled curve construction...
1-D solver tests
- [x] Testing Brent solver...
- [x] Testing bisection solver...
- [x] Testing false-position solver...
- [x] Testing Newton solver...
- [x] Testing Newton-safe solver...
- [x] Testing Halley solver...
- [x] Testing Halley-safe solver...
- [x] Testing finite-difference Newton-safe solver...
- [x] Testing Ridder solver...
- [x] Testing secant solver...
Factorial tests
- [x] Testing factorial numbers...
- [x] Testing Gamma function...
- [x] Testing Gamma values...
- [x] Testing modified Bessel function of first and second kind...
- [x] Testing weighted modified Bessel functions...
transformed grid
- [x] Testing transformed grid construction...
Distribution tests
- [x] Testing normal distributions...
- [x] Testing bivariate cumulative normal distribution...
- [x] Testing Poisson distribution...
- [x] Testing cumulative Poisson distribution...
- [x] Testing inverse cumulative Poisson distribution...
- [x] Testing bivariate cumulative Student t distribution...
- [x] Testing bivariate cumulative Student t distribution for large N...
- [x] Testing inverse CDF based on stochastic collocation...
linear least squares regression tests
- [x] Testing linear least-squares regression...
- [x] Testing multi-dimensional linear least-squares regression...
- [x] Testing 1D simple linear least-squares regression...
Statistics tests
- [x] Testing statistics...
- [x] Testing sequence statistics...
- [x] Testing convergence statistics...
- [x] Testing incremental statistics...
TQR eigendecomposition tests
- [x] Testing TQR eigenvalue decomposition...
- [x] Testing TQR zero-off-diagonal eigenvalues...
- [x] Testing TQR eigenvector decomposition...
Gaussian quadratures tests
- [x] Testing Gauss-Jacobi integration...
- [x] Testing Gauss-Laguerre integration...
- [x] Testing Gauss-Hermite integration...
- [x] Testing Gauss hyperbolic integration...
- [x] Testing tabulated Gauss-Laguerre integration...
Gaussian quadratures experimental tests
- [x] Testing Gauss non-central chi-squared integration...
- [x] Testing Gauss non-central chi-squared sum of notes...
Interpolation tests
- [x] Testing spline approximation on Gaussian data sets...
- [x] Testing spline interpolation on a Gaussian data set...
- [x] Testing spline interpolation on RPN15A data set...
- [x] Testing spline interpolation on generic values...
- [x] Testing symmetry of spline interpolation end-conditions ...
- [x] Testing derivative end-conditions for spline interpolation ...
- [x] Testing non-restrictive Hyman filter...
- [ ] Testing N-dimensional cubic spline...
- [x] Testing use of interpolations as functors...
- [x] Testing Fritsch-Butland interpolation...
- [x] Testing backward-flat interpolation...
- [x] Testing forward-flat interpolation...
- [x] Testing Sabr interpolation...
- [x] Testing kernel 1D interpolation...
- [x] Testing kernel 2D interpolation...
- [x] Testing bicubic spline derivatives...
- [x] Testing that bicubic splines actually update...
- [x] Testing Richardson extrapolation...
- [ ] Testing no-arbitrage Sabr interpolation...
- [ ] Testing Sabr calibration single cases...
- [x] Testing Sabr and no-arbitrage Sabr transformation functions...
- [x] Testing Lagrange interpolation...
- [x] Testing Lagrange interpolation at supporting points...
- [x] Testing Lagrange interpolation derivatives...
- [x] Testing Lagrange interpolation on Chebyshev points...
- [x] Testing B-Splines...
- [x] Testing piecewise constant interpolation on a single point...
Instrument tests
- [x] Testing observability of instruments...
- [x] Testing reaction of composite instrument to date changes...
Swap tests
- [x] Testing vanilla-swap calculation of fair fixed rate...
- [x] Testing vanilla-swap calculation of fair floating spread...
- [x] Testing vanilla-swap dependency on fixed rate...
- [x] Testing vanilla-swap dependency on floating spread...
- [x] Testing in-arrears swap calculation...
- [x] Testing vanilla-swap calculation against cached value...
Term structure tests
- [x] Testing term structure against evaluation date change...
- [x] Testing consistency of implied term structure...
- [x] Testing observability of implied term structure...
- [x] Testing consistency of forward-spreaded term structure...
- [x] Testing observability of forward-spreaded term structure...
- [x] Testing consistency of zero-spreaded term structure...
- [x] Testing observability of zero-spreaded term structure...
- [x] Testing that a zero-spreaded curve can be created with a null underlying curve...
- [x] Testing that an underlying curve can be relinked to a null underlying curve...
- [x] Testing composite zero yield structures...
Amortizing Bond tests
- [x] Testing amortizing fixed rate bond...
forward rate agreement
- [x] Testing forward rate agreement construction...
Quote tests
- [x] Testing observability of quotes...
- [x] Testing observability of quote handles...
- [x] Testing derived quotes...
- [x] Testing composite quotes...
- [x] Testing forward-value and implied-standard-deviation quotes...

## release note
* 0.2.3 fix `Term structure tests`, `Gaussian quadratures experimental tests`
