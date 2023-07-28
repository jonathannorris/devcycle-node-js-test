## DevCycle NodeJS Benchmark Testing

quick test app to benchmark and test the DevCycle NodeJS Server SDK.

### Build and Run

- set your DevCycle SDK Key as an environment variable: `DEVCYCLE_SERVER_SDK_KEY`
- if you would like to keep debug logs enabled (`logLevel: 'debug'`), you will need to change the following line in: `node_modules/@devcycle/nodejs-server-sdk/src/bucketing.js`
```javascript
- const debugWASM = (options === null || options === void 0 ? void 0 : options.logLevel) === 'debug';
+ const debugWASM = false;
```
- Run the script with: `DVC_BENCH_LOOP=1 node index.js`
- You should see regular `[DevCycle]: Flush Payloads:` logs flushing event payloads.
