# nem2-sdk-browserify
this is nemtech/nem2-sdk-typescript-javascript for browser

## how to use

```
<script src="nem2-sdk-0.13.0.js"></script>
```

```
const nem = require("/node_modules/nem2-sdk");
const rxjs = require("/node_modules/rxjs/operators");
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

```
