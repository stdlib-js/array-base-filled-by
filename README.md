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


<details>
  <summary>
    About stdlib...
  </summary>
  <p>We believe in a future in which the web is a preferred environment for numerical computation. To help realize this future, we've built stdlib. stdlib is a standard library, with an emphasis on numerical and scientific computation, written in JavaScript (and C) for execution in browsers and in Node.js.</p>
  <p>The library is fully decomposable, being architected in such a way that you can swap out and mix and match APIs and functionality to cater to your exact preferences and use cases.</p>
  <p>When you use stdlib, you can be absolutely certain that you are using the most thorough, rigorous, well-written, studied, documented, tested, measured, and high-quality code out there.</p>
  <p>To join us in bringing numerical computing to the web, get started by checking us out on <a href="https://github.com/stdlib-js/stdlib">GitHub</a>, and please consider <a href="https://opencollective.com/stdlib">financially supporting stdlib</a>. We greatly appreciate your continued support!</p>
</details>

# filledBy

[![NPM version][npm-image]][npm-url] [![Build Status][test-image]][test-url] [![Coverage Status][coverage-image]][coverage-url] <!-- [![dependencies][dependencies-image]][dependencies-url] -->

> Create a filled "generic" array according to a provided callback function.

<!-- Section to include introductory text. Make sure to keep an empty line after the intro `section` element and another before the `/section` close. -->

<section class="intro">

</section>

<!-- /.intro -->

<!-- Package usage documentation. -->



<section class="usage">

## Usage

```javascript
import filledBy from 'https://cdn.jsdelivr.net/gh/stdlib-js/array-base-filled-by@deno/mod.js';
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
import constantFunction from 'https://cdn.jsdelivr.net/gh/stdlib-js/utils-constant-function@deno/mod.js';
import filledBy from 'https://cdn.jsdelivr.net/gh/stdlib-js/array-base-filled-by@deno/mod.js';

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

This package is part of [stdlib][stdlib], a standard library with an emphasis on numerical and scientific computing. The library provides a collection of robust, high performance libraries for mathematics, statistics, streams, utilities, and more.

For more information on the project, filing bug reports and feature requests, and guidance on how to develop [stdlib][stdlib], see the main project [repository][stdlib].

#### Community

[![Chat][chat-image]][chat-url]

---

## License

See [LICENSE][stdlib-license].


## Copyright

Copyright &copy; 2016-2024. The Stdlib [Authors][stdlib-authors].

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

[chat-image]: https://img.shields.io/gitter/room/stdlib-js/stdlib.svg
[chat-url]: https://app.gitter.im/#/room/#stdlib-js_stdlib:gitter.im

[stdlib]: https://github.com/stdlib-js/stdlib

[stdlib-authors]: https://github.com/stdlib-js/stdlib/graphs/contributors

[umd]: https://github.com/umdjs/umd
[es-module]: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Modules

[deno-url]: https://github.com/stdlib-js/array-base-filled-by/tree/deno
[deno-readme]: https://github.com/stdlib-js/array-base-filled-by/blob/deno/README.md
[umd-url]: https://github.com/stdlib-js/array-base-filled-by/tree/umd
[umd-readme]: https://github.com/stdlib-js/array-base-filled-by/blob/umd/README.md
[esm-url]: https://github.com/stdlib-js/array-base-filled-by/tree/esm
[esm-readme]: https://github.com/stdlib-js/array-base-filled-by/blob/esm/README.md
[branches-url]: https://github.com/stdlib-js/array-base-filled-by/blob/main/branches.md

[stdlib-license]: https://raw.githubusercontent.com/stdlib-js/array-base-filled-by/main/LICENSE

</section>

<!-- /.links -->
