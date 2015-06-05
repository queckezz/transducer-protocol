# transducer-protocol

[![stable](http://badges.github.io/stability-badges/dist/stable.svg)](http://github.com/badges/stability-badges)

Official protocol for transducers based on [this spec](https://github.com/cognitect-labs/transducers-js#transformer-protocol).

## Usage

[![NPM](https://nodei.co/npm/transducer-protocol.png)](https://www.npmjs.com/package/transducer-protocol)

### Reduced implementation

where `p` is the protocol.

```js
const Reduced = value => {
  return {
    [p.value]: value,
    [p.reduced]: true
  }
}
```

### Transformer implementation

```js
const transformer = () => {
    return {
        [p.init]: init ? () => init : notSupported,
        [p.step]: step,
        [p.result]: identity
     }
 }
```

### Protocol

* protocol.init
* protocol.step
* protocol.result
* protocol.reduced
* protocol.value

## License

MIT, see [license.md](http://github.com/queckezz/transducer-protocol/blob/master/license.md) for details.
