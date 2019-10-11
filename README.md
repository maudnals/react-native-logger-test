# react-native-logger-test
Test app to reproduce logger issue as documented at https://github.com/mreuvers/typescript-logging/issues/43.

* clone
* `yarn`
* `yarn start`
* `react-native run-ios`
* Error:

```bash
Requiring module "node_modules/typescript-logging/dist/commonjs/typescript-logging.js", which threw an exception: TypeError: window.removeEventListener is not a function. (In 'window.removeEventListener("message", listener)', 'window.removeEventListener' is undefined)
loadModuleImplementation
    require.js:269:27
<global>
    App.js:9:1
loadModuleImplementation
    require.js:322:6
guardedLoadModule
    require.js:201:45
runUpdatedModule
    require.js:657:17
metroHotUpdateModule
    require.js:533:8
define
    require.js:53:24
global code
    App.bundle?platform=ios&dev=true&minify=false&modulesOnly=true&runModule=false&shallow=true:1:4
<unknown>
    [native code]:0
inject
    injectUpdate.js:62:35
forEach
    [native code]:0
injectUpdate
    injectUpdate.js:71:26
on$argument_1
    HMRClient.js:40:21
emit
    index.js:202:37
_ws.onmessage
    WebSocketHMRClient.js:72:20
EventTarget.prototype.dispatchEvent
    event-target-shim.js:818:39
_eventEmitter.addListener$argument_1
    WebSocket.js:232:27
emit
    EventEmitter.js:190:12
callFunctionReturnFlushedQueue
    [native code]:0
```


