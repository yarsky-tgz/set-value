# vue-set-value 

> Create nested values and any intermediaries on vue reactive objects using dot notation (`'a.b.c'`) paths.

This project is only fork of great package [set-value](https://github.com/jonschlinkert/set-value) made by [Jon Schlinkert](https://github.com/jonschlinkert)

## Install

Install with [npm](https://www.npmjs.com/):

```sh
$ npm install --save vue-set-value
```

## Usage

```js
var vueDeepSet = require('vue-set-value');
vueDeepSet(object, prop, value);
```

### Params

* `object` **{object}**: The object to set `value` on
* `prop` **{string}**: The property to set. Dot-notation may be used.
* `value` **{any}**: The value to set on `object[prop]`

## Examples

Updates and returns the given object:

```js
vueDeepSet(target, 'a.b.c', 'd');
console.log(target);
//=> { a: { b: { c: 'd' } } }
```

### Escaping

**Escaping with backslashes**

Prevent set-value from splitting on a dot by prefixing it with backslashes:

```js
console.log(vueDeepSet(target, 'a\\.b.c', 'd'));
//=> { 'a.b': { c: 'd' } }

console.log(vueDeepSet(target, 'a\\.b\\.c', 'd'));
//=> { 'a.b.c': 'd' }
```

### License

Copyright © 2018, [Yaroslav Dobzhanskij](https://github.com/yarsky-tgz).
Copyright © 2018, [Jon Schlinkert](https://github.com/jonschlinkert).
Released under the [MIT License](LICENSE).
