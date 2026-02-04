<!--

@license Apache-2.0

Copyright (c) 2024 The Stdlib Authors.

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

   http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.

-->


<details>
  <summary>
    About stdlib...
  </summary>
  <p>We believe in a future in which the web is a preferred environment for numerical computation. To help realize this future, we've built stdlib. stdlib is a standard library, with an emphasis on numerical and scientific computation, written in JavaScript (and C) for execution in browsers and in Node.js.</p>
  <p>The library is fully decomposable, being architected in such a way that you can swap out and mix and match APIs and functionality to cater to your exact preferences and use cases.</p>
  <p>When you use stdlib, you can be absolutely certain that you are using the most thorough, rigorous, well-written, studied, documented, tested, measured, and high-quality code out there.</p>
  <p>To join us in bringing numerical computing to the web, get started by checking us out on <a href="https://github.com/stdlib-js/stdlib">GitHub</a>, and please consider <a href="https://opencollective.com/stdlib">financially supporting stdlib</a>. We greatly appreciate your continued support!</p>
</details>

# kernelLog1p

[![NPM version][npm-image]][npm-url] [![Build Status][test-image]][test-url] [![Coverage Status][coverage-image]][coverage-url] <!-- [![dependencies][dependencies-image]][dependencies-url] -->

> Evaluate a correction term for double-precision base-2 and base-10 logarithms when `1+f` is in `[√2/2, √2]`.



<section class="usage">

## Usage

```javascript
import kernelLog1p from 'https://cdn.jsdelivr.net/gh/stdlib-js/math-base-special-kernel-log1p@deno/mod.js';
```

#### kernelLog1p( f )

Evaluates a correction term for double-precision base-2 and base-10 logarithms when `1+f` is in `[√2/2, √2]`.

```javascript
var v = kernelLog1p( 1.0 );
// returns ~0.1931

v = kernelLog1p( 1.4142135623730951 );
// returns ~0.4672

v = kernelLog1p( NaN );
// returns NaN
```

</section>

<!-- /.usage -->

<section class="notes">

## Notes

-   This function is a helper function for computing logarithms in base `e`. Argument reduction and adding the final term of the polynomial must be done by the caller for increased accuracy when different bases are used. For reference, see [`@stdlib/math-base/special/log2`][@stdlib/math/base/special/log2] and [`@stdlib/math/base/special/log10`][@stdlib/math/base/special/log10].

</section>

<!-- /.notes -->

<section class="examples">

## Examples

<!-- eslint no-undef: "error" -->

```javascript
import uniform from 'https://cdn.jsdelivr.net/gh/stdlib-js/random-array-uniform@deno/mod.js';
import logEachMap from 'https://cdn.jsdelivr.net/gh/stdlib-js/console-log-each-map@deno/mod.js';
import sqrt from 'https://cdn.jsdelivr.net/gh/stdlib-js/math-base-special-sqrt@deno/mod.js';
import kernelLog1p from 'https://cdn.jsdelivr.net/gh/stdlib-js/math-base-special-kernel-log1p@deno/mod.js';

var opts = {
    'dtype': 'float64'
};
var x = uniform( 100, sqrt( 2.0 ) / 2.0, sqrt( 2.0 ), opts );

logEachMap( 'kernelLog1p(%0.4f) = %0.4f', x, kernelLog1p );
```

</section>

<!-- /.examples -->

<!-- C interface documentation. -->



<!-- Section for related `stdlib` packages. Do not manually edit this section, as it is automatically populated. -->

<section class="related">

* * *

## See Also

-   <span class="package-name">[`@stdlib/math-base/special/log1p`][@stdlib/math/base/special/log1p]</span><span class="delimiter">: </span><span class="description">evaluate the natural logarithm of 1+x.</span>

</section>

<!-- /.related -->

<!-- Section for all links. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->


<section class="main-repo" >

* * *

## Notice

This package is part of [stdlib][stdlib], a standard library with an emphasis on numerical and scientific computing. The library provides a collection of robust, high performance libraries for mathematics, statistics, streams, utilities, and more.

For more information on the project, filing bug reports and feature requests, and guidance on how to develop [stdlib][stdlib], see the main project [repository][stdlib].

#### Community

[![Chat][chat-image]][chat-url]

---

## Copyright

Copyright &copy; 2016-2026. The Stdlib [Authors][stdlib-authors].

</section>

<!-- /.stdlib -->

<!-- Section for all links. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->

<section class="links">

[npm-image]: http://img.shields.io/npm/v/@stdlib/math-base-special-kernel-log1p.svg
[npm-url]: https://npmjs.org/package/@stdlib/math-base-special-kernel-log1p

[test-image]: https://github.com/stdlib-js/math-base-special-kernel-log1p/actions/workflows/test.yml/badge.svg?branch=v0.0.3
[test-url]: https://github.com/stdlib-js/math-base-special-kernel-log1p/actions/workflows/test.yml?query=branch:v0.0.3

[coverage-image]: https://img.shields.io/codecov/c/github/stdlib-js/math-base-special-kernel-log1p/main.svg
[coverage-url]: https://codecov.io/github/stdlib-js/math-base-special-kernel-log1p?branch=main

<!--

[dependencies-image]: https://img.shields.io/david/stdlib-js/math-base-special-kernel-log1p.svg
[dependencies-url]: https://david-dm.org/stdlib-js/math-base-special-kernel-log1p/main

-->

[chat-image]: https://img.shields.io/badge/zulip-join_chat-brightgreen.svg
[chat-url]: https://stdlib.zulipchat.com

[stdlib]: https://github.com/stdlib-js/stdlib

[stdlib-authors]: https://github.com/stdlib-js/stdlib/graphs/contributors

[umd]: https://github.com/umdjs/umd
[es-module]: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Modules

[deno-url]: https://github.com/stdlib-js/math-base-special-kernel-log1p/tree/deno
[deno-readme]: https://github.com/stdlib-js/math-base-special-kernel-log1p/blob/deno/README.md
[umd-url]: https://github.com/stdlib-js/math-base-special-kernel-log1p/tree/umd
[umd-readme]: https://github.com/stdlib-js/math-base-special-kernel-log1p/blob/umd/README.md
[esm-url]: https://github.com/stdlib-js/math-base-special-kernel-log1p/tree/esm
[esm-readme]: https://github.com/stdlib-js/math-base-special-kernel-log1p/blob/esm/README.md
[branches-url]: https://github.com/stdlib-js/math-base-special-kernel-log1p/blob/main/branches.md

[@stdlib/math/base/special/log2]: https://github.com/stdlib-js/math-base-special-log2/tree/deno

[@stdlib/math/base/special/log10]: https://github.com/stdlib-js/math-base-special-log10/tree/deno

<!-- <related-links> -->

[@stdlib/math/base/special/log1p]: https://github.com/stdlib-js/math-base-special-log1p/tree/deno

<!-- </related-links> -->

</section>

<!-- /.links -->
