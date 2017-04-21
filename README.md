# jwt-wrapper

this package is a wrapper to jsonwebtoken as promise

Consult [node-jsonwebtoken](https://github.com/auth0/node-jsonwebtoken) for detailed documentation.

## examples

### jwt.sign(payload, key, [options])

Sign a token with key, with options defaulting to `{ algorithm: 'HS256' }`.

ES6:

```js
jwt.sign({ username: 'myname' }, 'secret-dev-key').then(console.log)
```

ES7:

```js
const token = await jwt.sign({ username: 'myname' }, 'secret-dev-key')
console.log(token)
```

### jwt.verify(token, key, [options])

Verify a token, with options defaulting to `{ algorithm: 'HS256' }`.

ES6:

```js
jwt.verify(token, 'secret-dev-key')
  .then(console.log)
```

ES7:

```js
const token = await jwt.verify({ username: 'fl0w' }, 'secret-dev-key')
console.log(token)
