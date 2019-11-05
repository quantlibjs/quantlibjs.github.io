# quantlib.js [![npm version](https://img.shields.io/npm/v/@quantlib/ql.svg?style=flat)](https://www.npmjs.com/package/@quantlib/ql) [![](https://data.jsdelivr.com/v1/package/npm/@quantlib/ql/badge?style=rounded)](https://www.jsdelivr.com/package/npm/@quantlib/ql) [![License](https://img.shields.io/badge/License-Apache%202.0-blue.svg)](https://opensource.org/licenses/Apache-2.0)  [![copyright](https://img.shields.io/badge/%C2%A9%202019-Jin%20Yang-brightgreen)](https://quantlib.js.org/blog/) [![Twitter Follow](https://img.shields.io/twitter/follow/quantlibjs.svg?style=social&maxAge=3600)](https://twitter.com/quantlibjs)

## quantitative finance in javascript
1. [introduction](#introduction)
2. [get started](#get-started)
3. [how to use](#usage)
4. [release note](#release-note)
5. [api document](#docs)
6. [test suite & example](#test-suite--example)
7. [license](#license)
8. [credit](#credit)
9. [resource](#resource)
10. [test report](#test-report)
11. [example output](#example)

## introduction
`quantlib.js` aims to be a **COMPLETE** re-implementation of `C++` [QuantLib](https://quantlib.org) in `javascript` language, [emscripten](https://emscripten.org/) is **NOT** used. it can be used in web browser or node.js environment.

## get started

1. open https://quantlib.js.org with morden web browser, like chrome, firefox, etc...

2. select a `spec` or `example` from menu. `spec` source will be displayed on left panel, `spec` will be run with [jasmine](https://github.com/jasmine/jasmine) by your web browser, and test result will be displayed on right panel

## usage

#### load from cdn
* latest version: https://cdn.jsdelivr.net/npm/@quantlib/ql@latest/ql.mjs
* version `x.y.z` : https://cdn.jsdelivr.net/npm/@quantlib/ql@x.y.z/ql.mjs

#### install from npm

```
npm install @quantlib/ql
```

#### use in web page

`ql.mjs` is [ESM format](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Modules), when using in html script tag, make sure to have script type set to "module"

```html
<script type="module">
    import {someclass} from 'https://cdn.jsdelivr.net/npm/@quantlib/ql@latest/ql.mjs'
    const obj=new someclass();
    obj.dosomething();
</script>
```

#### use in node.js
`quantlib.js` works in `node.js` environment. after installing with `npm`, pass `--experimental-modules` to `node` to use ESM javascript file

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
`ql.d.ts` is published along with `ql.mjs`

```ts
import {someclass} from '@quantlib/ql'
const obj:someclass = new someclass();
obj.dosomething();
```

## release note
* 0.2.4 fix `risk statistics`, some `piecewise yield curve`
* 0.2.3 fix `Term structure tests`, `Gaussian quadratures experimental tests`

## docs
* https://quantlib.js.org/docs
* official c++ quantlib doc: https://www.quantlib.org/reference/

## test-suite & example

A static [report](https://quantlib.js.org/test-suite/) is updated regularly, so you could see the overall test status.

source code in ESM `javascript`:
* https://github.com/quantlibjs/test-suite
* https://github.com/quantlibjs/examples

converted from the `c++` [quantlib](https://www.quantlib.org/) [test-suite](https://github.com/lballabio/QuantLib/tree/master/test-suite) & [Examples](https://github.com/lballabio/QuantLib/tree/master/Examples)

these are the code loaded and executed in https://quantlib.js.org

## license
```

                                 Apache License
                           Version 2.0, January 2004
                        http://www.apache.org/licenses/

   TERMS AND CONDITIONS FOR USE, REPRODUCTION, AND DISTRIBUTION

   1. Definitions.

      "License" shall mean the terms and conditions for use, reproduction,
      and distribution as defined by Sections 1 through 9 of this document.

      "Licensor" shall mean the copyright owner or entity authorized by
      the copyright owner that is granting the License.

      "Legal Entity" shall mean the union of the acting entity and all
      other entities that control, are controlled by, or are under common
      control with that entity. For the purposes of this definition,
      "control" means (i) the power, direct or indirect, to cause the
      direction or management of such entity, whether by contract or
      otherwise, or (ii) ownership of fifty percent (50%) or more of the
      outstanding shares, or (iii) beneficial ownership of such entity.

      "You" (or "Your") shall mean an individual or Legal Entity
      exercising permissions granted by this License.

      "Source" form shall mean the preferred form for making modifications,
      including but not limited to software source code, documentation
      source, and configuration files.

      "Object" form shall mean any form resulting from mechanical
      transformation or translation of a Source form, including but
      not limited to compiled object code, generated documentation,
      and conversions to other media types.

      "Work" shall mean the work of authorship, whether in Source or
      Object form, made available under the License, as indicated by a
      copyright notice that is included in or attached to the work
      (an example is provided in the Appendix below).

      "Derivative Works" shall mean any work, whether in Source or Object
      form, that is based on (or derived from) the Work and for which the
      editorial revisions, annotations, elaborations, or other modifications
      represent, as a whole, an original work of authorship. For the purposes
      of this License, Derivative Works shall not include works that remain
      separable from, or merely link (or bind by name) to the interfaces of,
      the Work and Derivative Works thereof.

      "Contribution" shall mean any work of authorship, including
      the original version of the Work and any modifications or additions
      to that Work or Derivative Works thereof, that is intentionally
      submitted to Licensor for inclusion in the Work by the copyright owner
      or by an individual or Legal Entity authorized to submit on behalf of
      the copyright owner. For the purposes of this definition, "submitted"
      means any form of electronic, verbal, or written communication sent
      to the Licensor or its representatives, including but not limited to
      communication on electronic mailing lists, source code control systems,
      and issue tracking systems that are managed by, or on behalf of, the
      Licensor for the purpose of discussing and improving the Work, but
      excluding communication that is conspicuously marked or otherwise
      designated in writing by the copyright owner as "Not a Contribution."

      "Contributor" shall mean Licensor and any individual or Legal Entity
      on behalf of whom a Contribution has been received by Licensor and
      subsequently incorporated within the Work.

   2. Grant of Copyright License. Subject to the terms and conditions of
      this License, each Contributor hereby grants to You a perpetual,
      worldwide, non-exclusive, no-charge, royalty-free, irrevocable
      copyright license to reproduce, prepare Derivative Works of,
      publicly display, publicly perform, sublicense, and distribute the
      Work and such Derivative Works in Source or Object form.

   3. Grant of Patent License. Subject to the terms and conditions of
      this License, each Contributor hereby grants to You a perpetual,
      worldwide, non-exclusive, no-charge, royalty-free, irrevocable
      (except as stated in this section) patent license to make, have made,
      use, offer to sell, sell, import, and otherwise transfer the Work,
      where such license applies only to those patent claims licensable
      by such Contributor that are necessarily infringed by their
      Contribution(s) alone or by combination of their Contribution(s)
      with the Work to which such Contribution(s) was submitted. If You
      institute patent litigation against any entity (including a
      cross-claim or counterclaim in a lawsuit) alleging that the Work
      or a Contribution incorporated within the Work constitutes direct
      or contributory patent infringement, then any patent licenses
      granted to You under this License for that Work shall terminate
      as of the date such litigation is filed.

   4. Redistribution. You may reproduce and distribute copies of the
      Work or Derivative Works thereof in any medium, with or without
      modifications, and in Source or Object form, provided that You
      meet the following conditions:

      (a) You must give any other recipients of the Work or
          Derivative Works a copy of this License; and

      (b) You must cause any modified files to carry prominent notices
          stating that You changed the files; and

      (c) You must retain, in the Source form of any Derivative Works
          that You distribute, all copyright, patent, trademark, and
          attribution notices from the Source form of the Work,
          excluding those notices that do not pertain to any part of
          the Derivative Works; and

      (d) If the Work includes a "NOTICE" text file as part of its
          distribution, then any Derivative Works that You distribute must
          include a readable copy of the attribution notices contained
          within such NOTICE file, excluding those notices that do not
          pertain to any part of the Derivative Works, in at least one
          of the following places: within a NOTICE text file distributed
          as part of the Derivative Works; within the Source form or
          documentation, if provided along with the Derivative Works; or,
          within a display generated by the Derivative Works, if and
          wherever such third-party notices normally appear. The contents
          of the NOTICE file are for informational purposes only and
          do not modify the License. You may add Your own attribution
          notices within Derivative Works that You distribute, alongside
          or as an addendum to the NOTICE text from the Work, provided
          that such additional attribution notices cannot be construed
          as modifying the License.

      You may add Your own copyright statement to Your modifications and
      may provide additional or different license terms and conditions
      for use, reproduction, or distribution of Your modifications, or
      for any such Derivative Works as a whole, provided Your use,
      reproduction, and distribution of the Work otherwise complies with
      the conditions stated in this License.

   5. Submission of Contributions. Unless You explicitly state otherwise,
      any Contribution intentionally submitted for inclusion in the Work
      by You to the Licensor shall be under the terms and conditions of
      this License, without any additional terms or conditions.
      Notwithstanding the above, nothing herein shall supersede or modify
      the terms of any separate license agreement you may have executed
      with Licensor regarding such Contributions.

   6. Trademarks. This License does not grant permission to use the trade
      names, trademarks, service marks, or product names of the Licensor,
      except as required for reasonable and customary use in describing the
      origin of the Work and reproducing the content of the NOTICE file.

   7. Disclaimer of Warranty. Unless required by applicable law or
      agreed to in writing, Licensor provides the Work (and each
      Contributor provides its Contributions) on an "AS IS" BASIS,
      WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or
      implied, including, without limitation, any warranties or conditions
      of TITLE, NON-INFRINGEMENT, MERCHANTABILITY, or FITNESS FOR A
      PARTICULAR PURPOSE. You are solely responsible for determining the
      appropriateness of using or redistributing the Work and assume any
      risks associated with Your exercise of permissions under this License.

   8. Limitation of Liability. In no event and under no legal theory,
      whether in tort (including negligence), contract, or otherwise,
      unless required by applicable law (such as deliberate and grossly
      negligent acts) or agreed to in writing, shall any Contributor be
      liable to You for damages, including any direct, indirect, special,
      incidental, or consequential damages of any character arising as a
      result of this License or out of the use or inability to use the
      Work (including but not limited to damages for loss of goodwill,
      work stoppage, computer failure or malfunction, or any and all
      other commercial damages or losses), even if such Contributor
      has been advised of the possibility of such damages.

   9. Accepting Warranty or Additional Liability. While redistributing
      the Work or Derivative Works thereof, You may choose to offer,
      and charge a fee for, acceptance of support, warranty, indemnity,
      or other liability obligations and/or rights consistent with this
      License. However, in accepting such obligations, You may act only
      on Your own behalf and on Your sole responsibility, not on behalf
      of any other Contributor, and only if You agree to indemnify,
      defend, and hold each Contributor harmless for any liability
      incurred by, or claims asserted against, such Contributor by reason
      of your accepting any such warranty or additional liability.

   END OF TERMS AND CONDITIONS

   APPENDIX: How to apply the Apache License to your work.

      To apply the Apache License to your work, attach the following
      boilerplate notice, with the fields enclosed by brackets "[]"
      replaced with your own identifying information. (Don't include
      the brackets!)  The text should be enclosed in the appropriate
      comment syntax for the file format. We also recommend that a
      file or class name and description of purpose be included on the
      same "printed page" as the copyright notice for easier
      identification within third-party archives.

   Copyright [yyyy] [name of copyright owner]

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       http://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.
```

## credit

* C++ QuantLib project: https://quantlib.org
* C++ QuantLib-noboost: https://github.com/haozhangphd/QuantLib-noBoost
* mathjs: https://mathjs.org
* phosphor: https://github.com/phosphorjs/phosphor
* js.org: https://github.com/js-org/js.org

## resource
* Google group: https://groups.google.com/d/forum/quantlibjs/
* Follow us on Twitter: [@quantlibjs](https://twitter.com/quantlibjs)
* Facebook page: https://www.facebook.com/quantlibjs/
* blog: https://quantlib.js.org/blog/
* notebook: https://observablehq.com/@quantlib

## test report
v0.2.4 total: 339, passed: 323, failed: 10, pending: 6

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

time series tests
- [x] Testing time series construction...
- [x] Testing time series interval price...
- [ ] Testing time series iterators...

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

Risk statistics tests
- [x] Testing risk measures...

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

Cash flows tests
- [x] Testing cash-flow settings...
- [x] Testing dynamic cast of coupon in Black pricer...
- [x] Testing default evaluation date in cashflows methods...
- [x] Testing ibor leg construction with null fixing days...
- [x] Testing irregular first coupon reference dates with end of month enabled...
- [x] Testing irregular last coupon reference dates with end of month enabled...
- [x] Testing leg construction with partial schedule...

Capped and floored coupon tests
- [x] Testing degenerate collared coupon...
- [x] Testing collared coupon against its decomposition...

Interest Rate tests
- [x] Testing interest-rate conversions...

Black formula tests
- [x] Testing Bachelier implied vol...
- [x] Testing Chambers-Nawalkha implied vol approximation...
- [x] Testing Radoicic-Stefanica implied vol approximation...
- [x] Testing Radoicic-Stefanica lower bound...
- [x] Testing implied volatility calculation via adaptive successive over-relaxation...

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

Bond tests
- [x] Testing consistency of bond price/yield calculation...
- [x] Testing consistency of bond price/ATM rate calculation...
- [x] Testing consistency of bond price/z-spread calculation...
- [x] Testing theoretical bond price/yield calculation...
- [x] Testing bond price/yield calculation against cached values...
- [x] Testing zero-coupon bond prices against cached values...
- [x] Testing fixed-coupon bond prices against cached values...
- [x] Testing floating-rate bond prices against cached values...
- [x] Testing Brazilian public bond prices against Andima cached values...
- [x] Testing ex-coupon UK Gilt price against market values...
- [x] Testing ex-coupon Australian bond price against market values...
- [x] Testing South African R2048 bond price using Schedule constructor with Date vector...
- [x] Testing Thirty/360 bond with settlement on 31st of the month...

Cap and floor tests
- [x] Testing cap/floor vega...
- [x] Testing cap/floor dependency on strike...
- [x] Testing consistency between cap, floor and collar...
- [x] Testing cap/floor parity...
- [x] Testing cap/floor ATM rate...
- [x] Testing implied term volatility for cap and floor...
- [x] Testing Black cap/floor price against cached values...

forward rate agreement
- [x] Testing forward rate agreement construction...

Quote tests
- [x] Testing observability of quotes...
- [x] Testing observability of quote handles...
- [x] Testing derived quotes...
- [x] Testing composite quotes...
- [x] Testing forward-value and implied-standard-deviation quotes...

Brownian bridge tests
- [x] Testing Brownian-bridge variates...
- [ ] Testing Brownian-bridge path generation...

Path generation tests
- [x] Testing 1-D path generation against cached values...
- [x] Testing n-D path generation against cached values...

Curve States tests
- [x] Testing constant-maturity-swap-market-model curve state...

Operator tests
- [x] Testing tridiagonal operator...
- [x] Testing differential operators...
- [x] Testing consistency of BSM operators...

Piecewise yield curve tests
- [ ] Testing consistency of piecewise-log-cubic discount curve...
- [x] Testing consistency of piecewise-log-linear discount curve...
- [x] Testing consistency of piecewise-linear discount curve...
- [x] Testing consistency of piecewise-log-linear zero-yield curve...
- [x] Testing consistency of piecewise-linear zero-yield curve...
- [ ] Testing consistency of piecewise-cubic zero-yield curve...
- [x] Testing consistency of piecewise-linear forward-rate curve...
- [x] Testing consistency of piecewise-flat forward-rate curve...
- [ ] Testing consistency of piecewise-cubic forward-rate curve...
- [x] Testing consistency of convex monotone forward-rate curve...
- [ ] Testing consistency of local-bootstrap algorithm...
- [x] Testing observability of piecewise yield curve...
- [ ] Testing use of today's LIBOR fixings in swap curve...
- [x] Testing bootstrap over JPY LIBOR swaps...
- [ ] Testing copying of discount curve...
- [ ] Testing copying of forward-rate curve...
- [ ] Testing copying of zero-rate curve...
- [x] Testing SwapRateHelper last relevant date...
- [ ] Testing bootstrap starting from bad guess...

Interpolated piecewise zero spreaded yield curve tests
- [x] Testing flat interpolation before the first spreaded date...
- [x] Testing flat interpolation after the last spreaded date...
- [x] Testing linear interpolation with more than two spreaded dates...
- [x] Testing linear interpolation between two dates...
- [x] Testing forward flat interpolation between two dates...
- [x] Testing backward flat interpolation between two dates...
- [x] Testing default interpolation between two dates...
- [x] Testing factory constructor with additional parameters...
- [x] Testing term structure max date...
- [x] Testing quote update...

Chooser option tests
- [x] Testing analytic simple chooser option...
- [x] Testing analytic complex chooser option...

Extensible option tests
- [x] Testing analytic engine for holder-extensible option...
- [x] Testing analytic engine for writer-extensible option...

Credit risk plus tests
- [x] Testing extended credit risk plus model against reference values...