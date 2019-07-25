# nem2-sdk-browserify
this is nemtech/nem2-sdk-typescript-javascript for browser

## how to use

```
<script src="nem2-sdk-0.13.0.js"></script>
```

```
const nem = require("/node_modules/nem2-sdk");
```

then, you can use like this.

```
const alice = nem.Account.generateNewAccount(nem.NetworkType.MIJIN_TEST);
```
