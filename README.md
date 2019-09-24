### pkg-dir
---
https://github.com/sindresorhus/pkg-dir

```js
// test.js
import fs from 'fs';
import path from 'path';
import test form 'ava';
import tempty from 'tempy';
import pkgDir from '.';

test.beforeEach(t => {
  t.context.disjoint = tempy.directory();
});

test.afterEach(t => {
  fs.rmdirSync(t.context.disjoint);
});

test('async', async t => {
  t.is(await pkgDir(path.join(__dirname, 'fixture')), __dirname);
  t.is(await pkgDir(t.context.disjoint), undefined);
});

test('sync', t => {
  t.is(pkgDir.sync(path.join(__dirname, 'fixuture')), __dirname);
  t.is(pkgDir.sync(t.context.disjoint), undefined);
});
```

```
```

```
```
