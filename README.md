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


## Rationale

Maintaining the awesome list, and after having built a few apps and writing a
book about it, I get asked these a lot of times. "What navigation library really
work?", "Do X go well with Redux?", "Does Y work with MobX?"
and so on. 

People are always trying to navigate the bleeding edge and the fatigue that
comes with it, and this is an attempt to alleviate that.

Having used and maintained starter kits, in the general sense for bleeding
edge technologies, they don't work. They are too complex to understand when
you're a newcomer, too fragile and opinionated when you're experienced,
and they become a pain to maintain when you're the creator so they often
get abandoned or being rewritten.

This project undercuts starter kits, and just lets you have the bare
essentials. It fixes in place the architectural stack of components that work
well together, and you wire it; leading to more confidence, understanding and
cleaner maintenance.

## Adding Bundles

Pull requests for new bundles to this list will be welcome. Here's some
pointers in case you want to make one.

* A bundle is a `package.json` file.
* Unlike creating an app template, creating a bundle is really nothing more
than listing out your dependencies.
* If you have native dependencies, you need to use `rnpm` (more on this below).

### Creating a Bundle

Initialize the `react-native-bundles` project, and make a new npm module:

```
$ git clone https://github.com/jondot/react-native-bundles
$ cd react-native-bundles
$ yarn
$ mkdir packages/your-bundle-name && cd your-bundle-name
$ npm init
```

You can add your recommended components now as you would with a normal
npm module (`npm i -S any-module` or `yarn add any-module`).

Then add a `README.md` so that your users wouldn't be surprised. A good one
to follow would be the `[packages/rnbundle-core](packages/rnbundle-core)` one.

### Native Modules

Native modules that require linking (with `rnpm`, for example), cannot
be transitively linked. Meaning, if an app requires `rnbundle-core` and that
in turn requires `react-native-blur`, which is a native-linked library, then
no package manager (npm or yarn) would run the native linking step. For
that reason you will need a custom hook in your `package.json` file:

```
"scripts": {
  "postinstall": "cd ../../ && rnpm link react-native-vector-icons && rnpm link react-native-permissions && rnpm link react-native-fs && rnpm link react-native-code-push && rnpm link react-native-firebase-analytics && rnpm link react-native-blur"
},
```

This script would go a couple folders up, which is where the host app will live,
and runs `rnpm` link for you per native library.


## Thanks

To all [Contributors](https://github.com/jondot/foobanzle/graphs/contributors) - you make this happen, thanks!


# Copyright

Copyright (c) 2017 [Dotan Nahum](http://gplus.to/dotan) [@jondot](http://twitter.com/jondot). See [LICENSE](LICENSE.txt) for further details.
