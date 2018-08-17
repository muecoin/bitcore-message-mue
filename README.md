# MonetaryUnit Message Verification and Signing for Bitcore-Mue


[![NPM Package](https://img.shields.io/npm/v/bitcore-message-mue.svg?style=flat-square)](https://www.npmjs.org/package/bitcore-message-mue)
[![Build Status](https://img.shields.io/travis/muecoin/bitcore-message-mue.svg?branch=master&style=flat-square)](https://travis-ci.org/muecoin/bitcore-message-mue)
[![Coverage Status](https://img.shields.io/coveralls/bitpay/bitcore-message-mue.svg?style=flat-square)](https://coveralls.io/r/muecoin/bitcore-message-mue?branch=master)

bitcore-message-mue adds support for verifying and signing monetaryunit messages in [Node.js](http://nodejs.org/) and web browsers.

See [the main muecore repo](https://github.com/muecoin/muecore) for more information.

## Getting Started

```sh
npm install bitcore-message-mue
```

```sh
bower install bitcore-message-mue
```

To sign a message:

```javascript
var bitcore = require('bitcore-lib-mue');
var Message = require('bitcore-message-mue');

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

See [CONTRIBUTING.md](https://github.com/muecoin/muecore/blob/master/CONTRIBUTING.md) on the main muecore repo for information about how to contribute.

## License

Code released under [the MIT license](https://github.com/bitpay/bitcore/blob/master/LICENSE).

Copyright 2013-2015 BitPay, Inc. Bitcore is a trademark maintained by BitPay, Inc.

