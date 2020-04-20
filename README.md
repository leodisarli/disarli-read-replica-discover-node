# read-replica-discover

**js to receive master URL database and return read replica URL based on parameters.**

## Installation
`npm install read-replica-discover`
 
## Basic Usage - With default options

```js
const ReadReplicaUrl = require('read-replica-discover');

var masterUrl = 'database.cluster-asr3asefaw3.region.vendor.com';
console.log(ReadReplicaUrl(masterUrl));
// result: database.cluster-ro-asr3asefaw3.region.vendor.com
```

## With modified options

```js
const ReadReplicaUrl = require('read-replica-discover');

options = {
  cluster_master: 'master',
  cluster_read: 'master-rr',
  database_read: 'rr',
}

var masterUrl = 'database.master-asr3asefaw3.region.vendor.com';
console.log(ReadReplicaUrl(masterUrl));
// result database.master-rr-asr3asefaw3.region.vendor.com
```

## Example
* `npm run example` or `node example/read-replica-example.js`
* Check [example code](https://github.com/leodisarli/disarli-read-replica-discover-node/master/example/read-replica-example.js). When you run the example you should have an output in console log.

## Test
* `mocha` or `npm test`
* Check [test folder](https://github.com/leodisarli/disarli-read-replica-discover-node/master/test).

## License
[MIT licensed](https://opensource.org/licenses/MIT) and all it's dependencies are MIT or BSD licensed.
