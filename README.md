# coverage-test

A simple [vue-cli](https://cli.vuejs.org) app using mocha/chai for unit tests.

The `HelloWorld.vue` component has been modified with an [optional chaining](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Optional_chaining) example.
Optional chaining works in development, produciton, and the mocha tests. However, when code coverage is added, the tests fail.

```shell
❯ npm run test:unit

> coverage-test@0.1.0 test:unit /Users/wtf8yn/src/tmp/coverage-test
> nyc --reporter=lcov --reporter=text vue-cli-service test:unit

Download the Vue Devtools extension for a better development experience:
https://github.com/vuejs/vue-devtools
You are running Vue in development mode.
Make sure to turn on production mode when deploying for production.
See more tips at https://vuejs.org/guide/deployment.html
 WEBPACK  Compiling...

  [=========================] 98% (after emitting)

 ERROR  Failed to compile with 1 errors

 error  in ./src/components/HelloWorld.vue?vue&type=script&lang=js&

Syntax Error: SyntaxError: Unexpected token (130:29)


 @ ./src/components/HelloWorld.vue?vue&type=script&lang=js& 11:42-384
 @ ./src/components/HelloWorld.vue
 @ ./tests/unit/example.spec.js
 @ ./node_modules/mochapack/lib/entry.js

  [=========================] 100% (completed)

 WEBPACK  Failed to compile with 1 error(s)

Error in ./src/components/HelloWorld.vue?vue&type=script&lang=js&

  Module build failed (from ./node_modules/istanbul-instrumenter-loader/dist/cjs.js):
  SyntaxError: Unexpected token (130:29)

 ERROR  mochapack exited with code 1.
----------|---------|----------|---------|---------|-------------------
File      | % Stmts | % Branch | % Funcs | % Lines | Uncovered Line #s
----------|---------|----------|---------|---------|-------------------
All files |       0 |        0 |       0 |       0 |
----------|---------|----------|---------|---------|-------------------
npm ERR! code ELIFECYCLE
npm ERR! errno 1
npm ERR! coverage-test@0.1.0 test:unit: `nyc --reporter=lcov --reporter=text vue-cli-service test:unit`
npm ERR! Exit status 1
npm ERR!
npm ERR! Failed at the coverage-test@0.1.0 test:unit script.
npm ERR! This is probably not a problem with npm. There is likely additional logging output above.

npm ERR! A complete log of this run can be found in:
npm ERR!     /Users/wtf8yn/.npm/_logs/2020-08-31T16_18_56_818Z-debug.log
```

## Project setup

```
npm install
```

### Compiles and hot-reloads for development

```
npm run serve
```

### Compiles and minifies for production

```
npm run build
```

### Run your unit tests

```
npm run test:unit
```

### Run your end-to-end tests

```
npm run test:e2e
```

### Lints and fixes files

```
npm run lint
```

### Customize configuration

See [Configuration Reference](https://cli.vuejs.org/config/).
