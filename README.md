# nem2-sdk-browserify
this is nemtech/nem2-sdk-typescript-javascript for browser

## how to use

```
<script src="nem2-sdk-0.15.0.js"></script>
```

```js
const nem = require("/node_modules/nem2-sdk");
const rxjs = require("/node_modules/rxjs/operators");
const sha3_256 = require("/node_modules/sha3_256").sha3_256;
```

then, you can use like this.

```js
//nem sample
const alice = nem.Account.generateNewAccount(nem.NetworkType.MIJIN_TEST);

//rxjs sample
listener
.confirmed(alice.address)
.pipe(
    rxjs.filter((tx) => tx.transactionInfo !== undefined && tx.transactionInfo.hash === lockSignedTx.hash),
    rxjs.mergeMap(ignored => transactionHttp.announceAggregateBonded(signedTx))
)
.subscribe(_ => console.log(_), err => console.error(err)
);

//sha3_256 sample
const hash = sha3_256.create();

```

## how to create bundle file

if you want to create bundle file yourself,

```
npm install browserify
npm install nem2-sdk@0.15.0
 browserify -r ./node_modules/nem2-sdk -r ./node_modules/rxjs/operators -r ./node_modules/js-sha3 -r ./node_modules/buffer -o nem2-sdk-0.15.0.js
```
