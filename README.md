<!--

@license Apache-2.0

Copyright (c) 2022 The Stdlib Authors.

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

# filledBy

[![NPM version][npm-image]][npm-url] [![Build Status][test-image]][test-url] [![Coverage Status][coverage-image]][coverage-url] <!-- [![dependencies][dependencies-image]][dependencies-url] -->

> Create a filled "generic" array according to a provided callback function.

<!-- Section to include introductory text. Make sure to keep an empty line after the intro `section` element and another before the `/section` close. -->

<section class="intro">

</section>

<!-- /.intro -->

<!-- Package usage documentation. -->

<section class="installation">

## Installation

```bash
npm install @stdlib/array-base-filled-by
```

Alternatively,

-   To load the package in a website via a `script` tag without installation and bundlers, use the [ES Module][es-module] available on the [`esm` branch][esm-url].
-   If you are using Deno, visit the [`deno` branch][deno-url].
-   For use in Observable, or in browser/node environments, use the [Universal Module Definition (UMD)][umd] build available on the [`umd` branch][umd-url].

</section>

<section class="usage">

## Usage

```javascript
var filledBy = require( '@stdlib/array-base-filled-by' );
```

#### filledBy( len, clbk\[, thisArg] )

Returns a filled "generic" array according to a provided callback function.

```javascript
function clbk( i ) {
    return i;
}

var out = filledBy( 3, clbk );
// returns [ 0, 1, 2 ]
```

When invoked, a callback function is provided a single argument:

-   **index**: the current array index.

To set the callback execution context, provide a `thisArg`.

<!-- eslint-disable no-invalid-this -->

```javascript
function clbk( i ) {
    this.count += 1;
    return i;
}

var ctx = {
    'count': 0
};

var out = filledBy( 3, clbk, ctx );
// returns [ 0, 1, 2 ];

var cnt = ctx.count;
// returns 3
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

<!-- eslint no-undef: "error" -->

```javascript
var constantFunction = require( '@stdlib/utils-constant-function' );
var filledBy = require( '@stdlib/array-base-filled-by' );

var out = filledBy( 3, constantFunction( 0.0 ) );
// returns [ 0.0, 0.0, 0.0 ]

out = filledBy( 3, constantFunction( 'beep' ) );
// returns [ 'beep', 'beep', 'beep' ]

out = filledBy( 3, constantFunction( null ) );
// returns [ null, null, null ]

out = filledBy( 3, constantFunction( true ) );
// returns [ true, true, true ]

out = filledBy( 3, constantFunction( void 0 ) );
// returns [ undefined, undefined, undefined ]
```

</section>

<!-- /.examples -->

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

Copyright &copy; 2016-2022. The Stdlib [Authors][stdlib-authors].

</section>

<!-- /.stdlib -->

<!-- Section for all links. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->

<section class="links">

[npm-image]: http://img.shields.io/npm/v/@stdlib/array-base-filled-by.svg
[npm-url]: https://npmjs.org/package/@stdlib/array-base-filled-by

[test-image]: https://github.com/stdlib-js/array-base-filled-by/actions/workflows/test.yml/badge.svg?branch=main
[test-url]: https://github.com/stdlib-js/array-base-filled-by/actions/workflows/test.yml?query=branch:main

[coverage-image]: https://img.shields.io/codecov/c/github/stdlib-js/array-base-filled-by/main.svg
[coverage-url]: https://codecov.io/github/stdlib-js/array-base-filled-by?branch=main

<!--

[dependencies-image]: https://img.shields.io/david/stdlib-js/array-base-filled-by.svg
[dependencies-url]: https://david-dm.org/stdlib-js/array-base-filled-by/main

-->

[umd]: https://github.com/umdjs/umd
[es-module]: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Modules

[deno-url]: https://github.com/stdlib-js/array-base-filled-by/tree/deno
[umd-url]: https://github.com/stdlib-js/array-base-filled-by/tree/umd
[esm-url]: https://github.com/stdlib-js/array-base-filled-by/tree/esm

[chat-image]: https://img.shields.io/gitter/room/stdlib-js/stdlib.svg
[chat-url]: https://gitter.im/stdlib-js/stdlib/

[stdlib]: https://github.com/stdlib-js/stdlib

[stdlib-authors]: https://github.com/stdlib-js/stdlib/graphs/contributors

[stdlib-license]: https://raw.githubusercontent.com/stdlib-js/array-base-filled-by/main/LICENSE

</section>

<!-- /.links -->