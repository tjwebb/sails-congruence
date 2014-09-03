# <img src="http://cdn.tjw.io/images/sails-logo.png" height='43px' />-congruence

Generate browser-compatible validator functions for Sails.js models. A [congruence](https://www.npmjs.org/package/congruence) extension.

[![NPM version][npm-image]][npm-url]
[![Build status][travis-image]][travis-url]
[![Dependency Status][daviddm-image]][daviddm-url]

## Install
```sh
$ npm install sails-congruence --save
```

## Usage
Create a validator function from a model, e.g. [Account](https://github.com/tjwebb/xtuple-api/blob/master/api/models/Account.js):

```js
var congruence = require('sails-congruence');
var validateAccount = congruence.getSailsValidator(Account);

var valid = validateAccount({
  name: 'myaccount',
  type: 'X'
})
// returns false. 'X' is not a valid account type
// https://github.com/tjwebb/xtuple-api/blob/master/api/models/Account.js#L17
```

## API

#### `.getSailsValidator(model)`
Generate a Sails.js validator function for the specified model

| @param | description |
|:---|:---|
| `model` | the model to create the validator function for |
| **@return** | description |
| `Function` | a function that will return true if model is valid, false otherwise

## License
MIT

[sails-logo]: http://cdn.tjw.io/images/sails-logo.png
[sails-url]: https://sailsjs.org
[npm-image]: https://img.shields.io/npm/v/sails-congruence.svg?style=flat
[npm-url]: https://npmjs.org/package/sails-congruence
[travis-image]: https://img.shields.io/travis/tjwebb/sails-congruence.svg?style=flat
[travis-url]: https://travis-ci.org/tjwebb/sails-congruence
[daviddm-image]: http://img.shields.io/david/tjwebb/sails-congruence.svg?style=flat
[daviddm-url]: https://david-dm.org/tjwebb/sails-congruence
