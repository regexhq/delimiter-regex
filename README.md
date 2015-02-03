# delimiter-regex [![NPM version](https://badge.fury.io/js/delimiter-regex.svg)](http://badge.fury.io/js/delimiter-regex)

> Create regex for template delimiters.

## Install with [npm](npmjs.org)

```bash
npm i delimiter-regex --save
```


## Usage

```js
var delims = require('delimiter-regex');
```

**Example**:

Get a regex for matching front-matter:

```js
delims('---', '---');
//=> /---\s*([\s\S]*?)\s*---/
```

If no args are passed, es6 delimiter regex is returned:

```js
delims();
//=> /\$\{\s*([\s\S]*?)\s*\}/
```

## Params

- **delimiters** `{String|Array}`: supports array format (`delims(['{{', '}}'])`) or list (`delims('{{', '}}')`)
- **options**: currently RegExp `flags` is the only option

**Flags example**

```js
delims('{{', '}}', {flags: 'gm'});
//=> /\{\{([^}}]*)\}\}/gm
```

## Run tests

```bash
npm test
```

## Contributing
Pull requests and stars are always welcome. For bugs and feature requests, [please create an issue](https://github.com/jonschlinkert/delimiter-regex/issues)

## Author

**Jon Schlinkert**
 
+ [github/jonschlinkert](https://github.com/jonschlinkert)
+ [twitter/jonschlinkert](http://twitter.com/jonschlinkert) 

## License
Copyright (c) 2014-2015 Jon Schlinkert  
Released under the MIT license

***

_This file was generated by [verb](https://github.com/assemble/verb) on February 02, 2015._
