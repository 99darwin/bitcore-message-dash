# Dash Message Verification and Signing for Bitcore-Dash


[![NPM Package](https://img.shields.io/npm/v/bitcore-message-divi.svg?style=flat-square)](https://www.npmjs.org/package/bitcore-message-divi)
[![Build Status](https://img.shields.io/travis/divicoin/bitcore-message-divi.svg?branch=master&style=flat-square)](https://travis-ci.org/divicoin/bitcore-message-divi)
[![Coverage Status](https://img.shields.io/coveralls/bitpay/bitcore-message-divi.svg?style=flat-square)](https://coveralls.io/r/divicoin/bitcore-message-divi?branch=master)

bitcore-message-divi adds support for verifying and signing divi messages in [Node.js](http://nodejs.org/) and web browsers.

See [the main bitcore-divi repo](https://github.com/divicoin/bitcore-divi) for more information.

## Getting Started

```sh
npm install bitcore-message-divi
```

```sh
bower install bitcore-message-divi
```

To sign a message:

```javascript
var bitcore = require('divicore-lib');
var Message = require('bitcore-message-divi');

var privateKey = bitcore.PrivateKey.fromWIF('cPBn5A4ikZvBTQ8D7NnvHZYCAxzDZ5Z2TSGW2LkyPiLxqYaJPBW4');
var signature = Message('hello, world').sign(privateKey);
```

To verify a message:

```javascript
var address = 'n1ZCYg9YXtB5XCZazLxSmPDa8iwJRZHhGx';
var signature = 'H/DIn8uA1scAuKLlCx+/9LnAcJtwQQ0PmcPrJUq90aboLv3fH5fFvY+vmbfOSFEtGarznYli6ShPr9RXwY9UrIY=';
var verified = Message('hello, world').verify(address, signature);
```

## Contributing

See [CONTRIBUTING.md](https://github.com/divicoin/bitcore-divi/blob/master/CONTRIBUTING.md) on the main bitcore-divi repo for information about how to contribute.

## License

Code released under [the MIT license](https://github.com/bitpay/bitcore/blob/master/LICENSE).

Copyright 2013-2015 BitPay, Inc. Bitcore is a trademark maintained by BitPay, Inc.

