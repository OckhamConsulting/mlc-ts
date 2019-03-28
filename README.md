**:warning: SOON TO BE DEPRECATED IN FAVOR OF https://github.com/OckhamConsulting/mlc-core/tree/master/packages/crypto - PLEASE SUBMIT PULL REQUESTS TO THE CORE V2 REPOSITORY :warning:***

![TSMLC Logo](./banner.png)

# TSMLC

> An MLC API wrapper, written in TypeScript to interact with MLC blockchain.

[![npm](https://img.shields.io/npm/dt/mlc-ts.svg)]()
[![npm](https://img.shields.io/npm/v/mlc-ts.svg)]()
[![license](https://img.shields.io/github/license/ockhamconsulting/mlc-ts.svg)]()

TSMLC is a library client designed to facilitate how you interact with the MLC blockchain.

## Why TypeScript

  * TypeScript is is a superset of JavaScript which mainly offers optional static typing, classes, and interfaces. The learning curve is not that steep.
  * Types are optional, TSMLC compiles into ES5 so you can work with both, ECMAScript or TypeScript.
  * A better development experience, including auto-complete and fully documented.

## Documentation

> [API documentation](https://ockhamconsulting.github.io/mlc-ts/) is hosted on github pages, and is generated from [TypeDoc](https://github.com/TypeStrong/typedoc).

## Installation

TSMLC is avaliable from `npm`.

```bash
yarn add mlc-ts
```

or

```bash
npm i mlc-ts --save
```

## Usage

For the best TypeScript experience, you should either use [Visual Studio Code](http://code.visualstudio.com/), or a [plug-in for your favorite text editor](https://github.com/Microsoft/TypeScript/wiki/TypeScript-Editor-Support).

### Basic Examples

> Get delegate list from Devnet network.

```js
import { Client, Network, NetworkType } from 'mlc-ts';

const devnet = Network.getDefault(NetworkType.Devnet);
const client = new Client(devnet);

client.delegate.list().subscribe((list) => {
  console.log(list);
});
```

> Get address from passphrase.

```js
import { PrivateKey } from 'mlc-ts/core';

// if no specify a second param, default is mainnet
const key = PrivateKey.fromSeed('my secret passphrase');
console.log(key.getPublicKey().getAddress()); // AaWU6X3pGdtSCK3s9weo9tjth64F3hixgT
```

For more examples please see documentation or look for tests in each directory.

## Running the tests

```bash
npm run test
```

## Security

If you discover a security vulnerability within this project, please send an e-mail to security@laroue.org. All security vulnerabilities will be promptly addressed.

## Contributing

  * If you find any bugs, submit an [issue](../../issues) or open [pull-request](../../pulls), helping us catch and fix them.
  * Engage with other users and developers on [MLC Slack](https://laroue.org/slack/).
  * Join the #development channel on Slack or contact our developer Luc (@gitockham).
  * [Contribute bounties](./CONTRIBUTING.md).

## Credits

**Lúcio Rubens** - [@luciorubeens](https://github.com/luciorubeens);
**Luc Talarico** - [@gitockham](https://github.com/gitockham);

## License

TSMLC is licensed under the MIT License - see the [LICENSE](./LICENSE) file for details.
