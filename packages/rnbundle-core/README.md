# Core

This bundle includes core components that we think should eventually appear
in every React Native app.

## Quick Start

Use `npm` (as of `yarn` v0.22 there's no support for `postinstall`):

    $ npm i -S rnbundle-core


If you use `yarn` and would like to lock a version, you should use it
on top of `npm`:

    $ yarn add rnbundle-core


This will install the bundled libraries and components, and will link
native resources and code using `rnpm`.

## What's Included?

- [`lodash`](https://www.npmjs.com/package/lodash) - self-explanatory.
- [`react-native-vector-icons`](https://www.npmjs.com/package/react-native-vector-icons) - shortcircuit needing custom assets with sets
of scalable standard icons.
- [`react-native-permissions`](https://www.npmjs.com/package/react-native-permissions) - ask all permission types with a single API.
- [`react-native-fs`](https://www.npmjs.com/package/react-native-fs) - access the device's filesystem.
- [`react-native-animatable`](https://www.npmjs.com/package/react-native-animatable) - Easy prepackaged animations.
- [`react-native-app-intro`](https://www.npmjs.com/package/react-native-app-intro) - Every app needs an intro.
- [`react-native-code-push`](https://www.npmjs.com/package/react-native-code-push) - Code push (needs configuration).
- [`react-native-firebase-analytics`](https://www.npmjs.com/package/react-native-firebase-analytics) - Analytics (needs configuration).

## Extra Configuration

- Firebase needs an SDK. See more [here](https://github.com/evollu/react-native-fcm#ios-configuration).
- Codepush needs an SDK and some manual work. See more [here](http://microsoft.github.io/code-push/docs/react-native.html#link-4).

