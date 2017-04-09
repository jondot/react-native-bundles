# Chat App Bundle

This bundle includes hand-picked React Native components and libraries that make up
a chat app.


## Quick Start


Use `npm` (as of `yarn` v0.22 there's no support for `postinstall`):

    $ npm i -S rnbundle-core rnbundle-chat-app


If you use `yarn` and would like to lock a version, you should use it
on top of `npm`:

    $ yarn add  rnbundle-core rnbundle-chat-app


This will install the bundled libraries and components, and will link
native resources and code using `rnpm`.

## What's Included?

- [`@exponent/ex-navigation`](https://www.npmjs.com/package/@exponent/ex-navigation) - Although depracated, still as of this writing (when `react-navigation` is at `beta-7`) is the best fit for complex navigation use cases (such as for a chat application).
- [`axios`](https://www.npmjs.com/package/axios) - Promise based network fetch with middleware and plugin support.
- [`react-native-contacts`](https://www.npmjs.com/package/react-native-contacts) - A chat app needs access to contacts.
- [`react-native-fcm`](https://www.npmjs.com/package/react-native-fcm) - Firebase push, works cross platform.
- [`react-native-gifted-chat`](https://www.npmjs.com/package/react-native-gifted-chat) - By now performance concerns have settled for this library and it makes the best fit.
- [`react-native-swipe-out`](https://www.npmjs.com/package/react-native-swipe-out) - For chat listing, handle actions such as archive etc. (like WhatsApp).
