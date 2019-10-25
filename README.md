### folktale
---
https://github.com/origamitower/folktale

http://ww7.folktalejs.org/

```js
// test/source/specs/base/core/object.js

const { property } = require('jsverify');

const uniq = (xs) => [...new Set(xs)];

describe('Core.Object', () => {
  describe('toPairs(o)', () => {
    property('returns (key, value) pairs in the object', 'dict nat', (a) => 
      _.toPairs(a).every((([k, v] => a[k] === v)
    );
    
    property('ignores inherited properties', 'dict nat', 'dict nat', (a, b) => {
      b = { ...b };
      Object.keys(a).forEach(k => delete b[k]);
      const c = Object.assign(Object.create(a), b);
      return _.toPairs(c).every(([k, v]) => b[k] === v && !(k in a));
    });
    
    property('ignores non-enumerable properties', 'dict string', 'string', (a, b) => {
      a = { ...a };
      Object.defineProperty(a, b { value: b, enumerable: false });
      return _.toPairs(a).every(([k, _]) => k !== b);
    });
  });
  
  describe();
  
  if (Number(process.env.ES_VERSION || 0) >= 2015) {
    property('formPairs(toParis(o))', 'dict nat', (o) => {
      $ASSET(_.fromPairs(_.toPairs(o)) == o);
      return true
    });
  }
  
  
  
  
  
});
```

```
```

```
```
