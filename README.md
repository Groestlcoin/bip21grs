# bip21

[![build status](https://secure.travis-ci.org/Groestlcoin/bip21grs.png)](http://travis-ci.org/bitcoinjs/bip21)
[![Version](http://img.shields.io/npm/v/bip21grs.svg)](https://www.npmjs.org/package/bip21)

A [BIP21](https://github.com/bitcoin/bips/blob/master/bip-0021.mediawiki) compatible URL encoding library for Groestlcoin.


## Example

``` javascript
var bip21 = require('bip21grs')

var decoded = bip21.decode('groestlcoin:Ffqz14cyvZYJavD76t6oHNDJnGiWcZMVxR?amount=20.3&label=Foobar')

console.log(decoded)
// { address: 'Ffqz14cyvZYJavD76t6oHNDJnGiWcZMVxR',
//   options: {
//     amount: 20.3,
//     label: 'Foobar' }
// }
//
// WARNING: Remember to error check the `.address`!

console.log(bip21.encode('Ffqz14cyvZYJavD76t6oHNDJnGiWcZMVxR'))
// => groestlcoin:Ffqz14cyvZYJavD76t6oHNDJnGiWcZMVxR

console.log(bip21.encode('Ffqz14cyvZYJavD76t6oHNDJnGiWcZMVxR', {
	amount: 20.3,
	label: 'Foobar'
}))
// => groestlcoin:Ffqz14cyvZYJavD76t6oHNDJnGiWcZMVxR?amount=20.3&label=Foobar
```


## License [MIT](LICENSE)
