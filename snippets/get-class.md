### Get the class of a variable

Use `Object.prototype.toString` to get the internal class or "type" of a variable. The return value (e.g. `[object Function]`) is cleaned up with a bit of `String.slice`.

```js
const getClass = v => Object.prototype.toString.call(v).slice(8, -1);
// getClass('foo') -> 'String'
// getClass(() => null) -> 'Function'
// getClass({}) -> 'Object'
```
