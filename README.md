<!--

@license Apache-2.0

Copyright (c) 2020 The Stdlib Authors.

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

# Strided Array Native Add-ons

[![NPM version][npm-image]][npm-url] [![Build Status][test-image]][test-url] [![Coverage Status][coverage-image]][coverage-url] <!-- [![dependencies][dependencies-image]][dependencies-url] -->

> C APIs for creating Node-API strided array native add-ons.

<!-- Section to include introductory text. Make sure to keep an empty line after the intro `section` element and another before the `/section` close. -->

<section class="intro">

This package exposes an absolute file path for the directory containing header files for various C APIs. The various C APIs facilitate the creation of Node-API strided array native add-ons.

</section>

<!-- /.intro -->

<!-- Package usage documentation. -->

<section class="installation">

## Installation

```bash
npm install @stdlib/strided-napi
```

</section>

<section class="usage">

## Usage

```javascript
var headerDir = require( '@stdlib/strided-napi' );
```

#### headerDir

Absolute file path for the directory containing header files for C APIs.

```javascript
var dir = headerDir;
// returns <string>
```

</section>

<!-- /.usage -->

<!-- Package usage notes. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->

<section class="notes">

</section>

<!-- /.notes -->

<!-- Package usage examples. -->

<section class="examples">

## Examples

```javascript
var headerDir = require( '@stdlib/strided-napi' );

console.log( headerDir );
// => <string>
```

</section>

<!-- /.examples -->

<!-- C interface documentation. -->

* * *

<section class="c">

## C APIs

<!-- Section to include introductory text. Make sure to keep an empty line after the intro `section` element and another before the `/section` close. -->

<section class="intro">

This package exposes various C APIs to facilitate the creation of Node-API strided array native add-ons. The included C APIs are the APIs implemented in the following packages:

<!-- NOTE: please keep in alphabetical order -->

-   [`@stdlib/strided-base/binary`][@stdlib/strided/base/binary]: strided array loops for operating on two input strided arrays and one or more output strided arrays.
-   [`@stdlib/strided-base/cmap`][@stdlib/strided/base/cmap]: single-precision complex floating-point strided array interface for applying a unary callback to a single input strided array.
-   [`@stdlib/strided-base/dmap`][@stdlib/strided/base/dmap]: double-precision floating-point strided array interface for applying a unary callback to a single input strided array.
-   [`@stdlib/strided-base/dmap2`][@stdlib/strided/base/dmap2]: double-precision floating-point strided array interface for applying a binary callback to two input strided arrays.
-   [`@stdlib/strided-base/dmskmap`][@stdlib/strided/base/dmskmap]: double-precision floating-point strided array interface for applying a unary callback to a single input strided array according to a mask strided array.
-   [`@stdlib/strided-base/dmskmap2`][@stdlib/strided/base/dmskmap2]: double-precision floating-point strided array interface for applying a unary callback to two input strided arrays according to a mask strided array.
-   [`@stdlib/strided-base/function-object`][@stdlib/strided/base/function-object]: strided array function object.
-   [`@stdlib/strided-base/mskunary`][@stdlib/strided/base/mskunary]: strided array loops for operating on a single input strided array, a mask strided array, and one or more output strided arrays.
-   [`@stdlib/strided-base/nullary`][@stdlib/strided/base/nullary]: strided array loops for operating on one or more output strided arrays.
-   [`@stdlib/strided-base/smap`][@stdlib/strided/base/smap]: single-precision floating-point strided array interface for applying a unary callback to a single input strided array.
-   [`@stdlib/strided-base/smap2`][@stdlib/strided/base/smap2]: single-precision floating-point strided array interface for applying a binary callback to two input strided arrays.
-   [`@stdlib/strided-base/smskmap`][@stdlib/strided/base/smskmap]: single-precision floating-point strided array interface for applying a unary callback to a single input strided array according to a mask strided array.
-   [`@stdlib/strided-base/smskmap2`][@stdlib/strided/base/smskmap2]: single-precision floating-point strided array interface for applying a unary callback to two input strided arrays according to a mask strided array.
-   [`@stdlib/strided-base/unary`][@stdlib/strided/base/unary]: strided array loops for operating on a single input strided array and one or more output strided arrays.
-   [`@stdlib/strided-base/zmap`][@stdlib/strided/base/zmap]: double-precision complex floating-point strided array interface for applying a unary callback to a single input strided array.
-   [`@stdlib/strided-dtypes`][@stdlib/strided/dtypes]: supported strided array data types.
-   [`@stdlib/strided-napi/binary`][@stdlib/strided/napi/binary]: Node-API interfaces and macros for registering one or more [`@stdlib/strided/base/binary`][@stdlib/strided/base/binary] interfaces with support for multiple dispatch.
-   [`@stdlib/strided-napi/cmap`][@stdlib/strided/napi/cmap]: Node-API interfaces and macros for registering a [`@stdlib/strided/base/cmap`][@stdlib/strided/base/cmap] function.
-   [`@stdlib/strided-napi/dmap`][@stdlib/strided/napi/dmap]: Node-API interfaces and macros for registering a [`@stdlib/strided/base/dmap`][@stdlib/strided/base/dmap] function.
-   [`@stdlib/strided-napi/dmap2`][@stdlib/strided/napi/dmap2]: Node-API interfaces and macros for registering a [`@stdlib/strided/base/dmap2`][@stdlib/strided/base/dmap2] function.
-   [`@stdlib/strided-napi/dmskmap`][@stdlib/strided/napi/dmskmap]: Node-API interfaces and macros for registering a [`@stdlib/strided/base/dmskmap`][@stdlib/strided/base/dmskmap] function.
-   [`@stdlib/strided-napi/dmskmap2`][@stdlib/strided/napi/dmskmap2]: Node-API interfaces and macros for registering a [`@stdlib/strided/base/dmskmap2`][@stdlib/strided/base/dmskmap2] function.
-   [`@stdlib/strided-napi/mskunary`][@stdlib/strided/napi/mskunary]: Node-API interfaces and macros for registering one or more [`@stdlib/strided/base/mskunary`][@stdlib/strided/base/mskunary] interfaces with support for multiple dispatch.
-   [`@stdlib/strided-napi/nullary`][@stdlib/strided/napi/nullary]: Node-API interfaces and macros for registering one or more [`@stdlib/strided/base/nullary`][@stdlib/strided/base/nullary] interfaces with support for multiple dispatch.
-   [`@stdlib/strided-napi/smap`][@stdlib/strided/napi/smap]: Node-API interfaces and macros for registering a [`@stdlib/strided/base/smap`][@stdlib/strided/base/smap] function.
-   [`@stdlib/strided-napi/smap2`][@stdlib/strided/napi/smap2]: Node-API interfaces and macros for registering a [`@stdlib/strided/base/smap2`][@stdlib/strided/base/smap2] function.
-   [`@stdlib/strided-napi/smskmap`][@stdlib/strided/napi/smskmap]: Node-API interfaces and macros for registering a [`@stdlib/strided/base/smskmap`][@stdlib/strided/base/smskmap] function.
-   [`@stdlib/strided-napi/smskmap2`][@stdlib/strided/napi/smskmap2]: Node-API interfaces and macros for registering a [`@stdlib/strided/base/smskmap2`][@stdlib/strided/base/smskmap2] function.
-   [`@stdlib/strided-napi/unary`][@stdlib/strided/napi/unary]: Node-API interfaces and macros for registering one or more [`@stdlib/strided/base/unary`][@stdlib/strided/base/unary] interfaces with support for multiple dispatch.
-   [`@stdlib/strided-napi/zmap`][@stdlib/strided/napi/zmap]: Node-API interfaces and macros for registering a [`@stdlib/strided/base/zmap`][@stdlib/strided/base/zmap] function.

For API documentation, consult the individual packages.

</section>

<!-- /.intro -->

<!-- C usage documentation. -->

<section class="usage">

### Usage

```c
#include "stdlib/strided/napi.h"
```

</section>

<!-- /.usage -->

<!-- C API usage notes. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->

<section class="notes">

</section>

<!-- /.notes -->

<!-- C API usage examples. -->

<section class="examples">

### Examples

```c
#include "stdlib/strided/napi.h"

static double identity( const double x ) {
    return x;
}

STDLIB_STRIDED_NAPI_MODULE_DMAP( identity )
```

</section>

<!-- /.examples -->

</section>

<!-- /.c -->

<!-- Section to include cited references. If references are included, add a horizontal rule *before* the section. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->

<section class="references">

</section>

<!-- /.references -->

<!-- Section for related `stdlib` packages. Do not manually edit this section, as it is automatically populated. -->

<section class="related">

</section>

<!-- /.related -->

<!-- Section for all links. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->


<section class="main-repo" >

* * *

## Notice

This package is part of [stdlib][stdlib], a standard library for JavaScript and Node.js, with an emphasis on numerical and scientific computing. The library provides a collection of robust, high performance libraries for mathematics, statistics, streams, utilities, and more.

For more information on the project, filing bug reports and feature requests, and guidance on how to develop [stdlib][stdlib], see the main project [repository][stdlib].

#### Community

[![Chat][chat-image]][chat-url]

---

## License

See [LICENSE][stdlib-license].


## Copyright

Copyright &copy; 2016-2025. The Stdlib [Authors][stdlib-authors].

</section>

<!-- /.stdlib -->

<!-- Section for all links. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->

<section class="links">

[npm-image]: http://img.shields.io/npm/v/@stdlib/strided-napi.svg
[npm-url]: https://npmjs.org/package/@stdlib/strided-napi

[test-image]: https://github.com/stdlib-js/strided-napi/actions/workflows/test.yml/badge.svg?branch=main
[test-url]: https://github.com/stdlib-js/strided-napi/actions/workflows/test.yml?query=branch:main

[coverage-image]: https://img.shields.io/codecov/c/github/stdlib-js/strided-napi/main.svg
[coverage-url]: https://codecov.io/github/stdlib-js/strided-napi?branch=main

<!--

[dependencies-image]: https://img.shields.io/david/stdlib-js/strided-napi.svg
[dependencies-url]: https://david-dm.org/stdlib-js/strided-napi/main

-->

[chat-image]: https://img.shields.io/gitter/room/stdlib-js/stdlib.svg
[chat-url]: https://app.gitter.im/#/room/#stdlib-js_stdlib:gitter.im

[stdlib]: https://github.com/stdlib-js/stdlib

[stdlib-authors]: https://github.com/stdlib-js/stdlib/graphs/contributors

[stdlib-license]: https://raw.githubusercontent.com/stdlib-js/strided-napi/main/LICENSE

[@stdlib/strided/base/binary]: https://github.com/stdlib-js/strided-base-binary

[@stdlib/strided/base/cmap]: https://github.com/stdlib-js/strided-base-cmap

[@stdlib/strided/base/dmap]: https://github.com/stdlib-js/strided-base-dmap

[@stdlib/strided/base/dmap2]: https://github.com/stdlib-js/strided-base-dmap2

[@stdlib/strided/base/dmskmap]: https://github.com/stdlib-js/strided-base-dmskmap

[@stdlib/strided/base/dmskmap2]: https://github.com/stdlib-js/strided-base-dmskmap2

[@stdlib/strided/base/function-object]: https://github.com/stdlib-js/strided-base-function-object

[@stdlib/strided/base/mskunary]: https://github.com/stdlib-js/strided-base-mskunary

[@stdlib/strided/base/nullary]: https://github.com/stdlib-js/strided-base-nullary

[@stdlib/strided/base/smap]: https://github.com/stdlib-js/strided-base-smap

[@stdlib/strided/base/smap2]: https://github.com/stdlib-js/strided-base-smap2

[@stdlib/strided/base/smskmap]: https://github.com/stdlib-js/strided-base-smskmap

[@stdlib/strided/base/smskmap2]: https://github.com/stdlib-js/strided-base-smskmap2

[@stdlib/strided/base/unary]: https://github.com/stdlib-js/strided-base-unary

[@stdlib/strided/base/zmap]: https://github.com/stdlib-js/strided-base-zmap

[@stdlib/strided/dtypes]: https://github.com/stdlib-js/strided-dtypes

[@stdlib/strided/napi/binary]: https://github.com/stdlib-js/strided-napi-binary

[@stdlib/strided/napi/cmap]: https://github.com/stdlib-js/strided-napi-cmap

[@stdlib/strided/napi/dmap]: https://github.com/stdlib-js/strided-napi-dmap

[@stdlib/strided/napi/dmap2]: https://github.com/stdlib-js/strided-napi-dmap2

[@stdlib/strided/napi/dmskmap]: https://github.com/stdlib-js/strided-napi-dmskmap

[@stdlib/strided/napi/dmskmap2]: https://github.com/stdlib-js/strided-napi-dmskmap2

[@stdlib/strided/napi/mskunary]: https://github.com/stdlib-js/strided-napi-mskunary

[@stdlib/strided/napi/nullary]: https://github.com/stdlib-js/strided-napi-nullary

[@stdlib/strided/napi/smap]: https://github.com/stdlib-js/strided-napi-smap

[@stdlib/strided/napi/smap2]: https://github.com/stdlib-js/strided-napi-smap2

[@stdlib/strided/napi/smskmap]: https://github.com/stdlib-js/strided-napi-smskmap

[@stdlib/strided/napi/smskmap2]: https://github.com/stdlib-js/strided-napi-smskmap2

[@stdlib/strided/napi/unary]: https://github.com/stdlib-js/strided-napi-unary

[@stdlib/strided/napi/zmap]: https://github.com/stdlib-js/strided-napi-zmap

</section>

<!-- /.links -->
