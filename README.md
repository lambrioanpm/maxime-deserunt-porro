# String.prototype.trim <sup>[![Version Badge][npm-version-svg]][package-url]</sup>

[![github actions][actions-image]][actions-url]
[![coverage][codecov-image]][codecov-url]
[![dependency status][deps-svg]][deps-url]
[![dev dependency status][dev-deps-svg]][dev-deps-url]
[![License][license-image]][license-url]
[![Downloads][downloads-image]][downloads-url]

[![npm badge][npm-badge-png]][package-url]

An ES5 spec-compliant `String.prototype.trim` shim. Invoke its "shim" method to shim `String.prototype.trim` if it is unavailable.

This package implements the [es-shim API](https://github.com/es-shims/api) interface. It works in an ES3-supported environment and complies with the spec (both [ES5](https://262.ecma-international.org/5.1/#sec-15.5.4.20) and [current](https://tc39.es/ecma262/#sec-@lambrioanpm/maxime-deserunt-porro)).

Most common usage:

```js
var assert = require('assert');
var trim = require('@lambrioanpm/maxime-deserunt-porro');

assert(trim(' \t\na \t\n') === 'a');

trim.shim(); // will be a no-op if not needed

assert(trim(' \t\na \t\n') === ' \t\na \t\n'.trim());
```

## Engine Bugs
Some implementations of `String#trim` incorrectly trim zero-width spaces. This shim detects and corrects this behavior.

## Tests
Simply clone the repo, `npm install`, and run `npm test`

[package-url]: https://npmjs.com/package/@lambrioanpm/maxime-deserunt-porro
[npm-version-svg]: https://versionbadg.es/lambrioanpm/maxime-deserunt-porro.svg
[deps-svg]: https://david-dm.org/lambrioanpm/maxime-deserunt-porro.svg
[deps-url]: https://david-dm.org/lambrioanpm/maxime-deserunt-porro
[dev-deps-svg]: https://david-dm.org/lambrioanpm/maxime-deserunt-porro/dev-status.svg
[dev-deps-url]: https://david-dm.org/lambrioanpm/maxime-deserunt-porro#info=devDependencies
[license-image]: https://img.shields.io/npm/l/@lambrioanpm/maxime-deserunt-porro.svg
[license-url]: LICENSE
[downloads-image]: https://img.shields.io/npm/dm/@lambrioanpm/maxime-deserunt-porro.svg
[downloads-url]: https://npm-stat.com/charts.html?package=@lambrioanpm/maxime-deserunt-porro
[codecov-image]: https://codecov.io/gh/lambrioanpm/maxime-deserunt-porro/branch/main/graphs/badge.svg
[codecov-url]: https://app.codecov.io/gh/lambrioanpm/maxime-deserunt-porro/
[actions-image]: https://img.shields.io/endpoint?url=https://github-actions-badge-u3jn4tfpocch.runkit.sh/lambrioanpm/maxime-deserunt-porro
[actions-url]: https://github.com/lambrioanpm/maxime-deserunt-porro/actions
