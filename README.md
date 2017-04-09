# React Native Bundles

Hand-picked bundles of React Native libraries and components that go well together for
any kind of app. Let's kill components fatigue!.

In other words, turn this:

```js
{
  // in package.json
  // ...
  "dependencies": {
    "@exponent/ex-navigation": "2.7.1",
    "@shoutem/ui": "^0.9.1",
    "axios": "^0.15.3",
    "faker": "^4.1.0",
    "firebase": "^3.7.1",
    "immutable": "^3.8.1",
    "lodash": "^4.16.6",
    "nachos-ui": "^0.1.2",
    "ramda": "^0.23.0",
    "react-native-app-intro": "^1.1.5",
    "react-native-code-push": "^1.15.0-beta",
    "react-native-contacts": "^0.7.1",
    "react-native-fabric": "0.4.0",
    // ...
  }
}
```

Into this:

```js
{
  // in package.json
  // ...
  "dependencies": {
    "rnbundle-core": "0.1.0",
    "rnbundle-redux": "0.1.0",
    "rnbundle-chat-app": "0.4.0",
  }
}
```

## Quick Start

Use `npm` (as of `yarn` v0.22 there's no support for `postinstall`):

    $ npm i -S rnbundle-core


If you use `yarn` and would like to lock a version, you should use it
on top of `npm`:

    $ yarn add rnbundle-core


This will install the bundled libraries and components, and will link
native resources and code using `rnpm`.


