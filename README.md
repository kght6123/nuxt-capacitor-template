# nuxt-capacitor-demo

> My splendiferous Nuxt.js project

## Capacitor For Android/iOS setup

このプロジェクトをCapacitor対応にセットアップして、AndroidとiOSのプロジェクトを作る方法

```
$ yarn create nuxt-app nuxt-capacitor-demo
yarn create v1.17.3
[1/4] 🔍  Resolving packages...
[2/4] 🚚  Fetching packages...
[3/4] 🔗  Linking dependencies...
warning "@vue/cli > @vue/cli-ui > graphql-tag@2.10.1" has unmet peer dependency "graphql@^0.9.0 || ^0.10.0 || ^0.11.0 || ^0.12.0 || ^0.13.0 || ^14.0.0".
warning "@vue/cli > @vue/cli-ui > graphql-type-json@0.2.1" has unmet peer dependency "graphql@>=0.8.0".
[4/4] 🔨  Building fresh packages...
success Installed "create-nuxt-app@2.10.1" with binaries:
      - create-nuxt-app

create-nuxt-app v2.10.1
✨  Generating Nuxt.js project in nuxt-capacitor-demo
? Project name nuxt-capacitor-demo
? Project description My splendiferous Nuxt.js project
? Author name kght6123
? Choose the package manager Yarn
? Choose UI framework Bootstrap Vue
? Choose custom server framework None (Recommended)
? Choose Nuxt.js modules Axios, Progressive Web App (PWA) Support
? Choose linting tools (Press <space> to select, <a> to toggle all, <i> to inver
t selection)
? Choose test framework None
? Choose rendering mode Single Page App
? Choose development tools jsconfig.json (Recommended for VS Code)

🎉  Successfully created project nuxt-capacitor-demo

  To get started:

	cd nuxt-capacitor-demo
	yarn dev

  To build & start for production:

	cd nuxt-capacitor-demo
	yarn build
	yarn start

✨  Done in 262.24s.

$ cd nuxt-capacitor-demo
$ code .
$ yarn add @capacitor/core @capacitor/cli
$ npx cap init
? App name NuxtCapacitorDemo
? App Package ID (in Java package format, no dashes) jp.kght6123.
nuxtcapacitordemo
⠋ Initializing Capacitor project in /Volumes/Develop/capacitor/nu✔ Initializing Capacitor project in /Volumes/Develop/capacitor/nuxt-capacitor-demo in 15.28ms


🎉   Your Capacitor project is ready to go!  🎉

Add platforms using "npx cap add":

  npx cap add android
  npx cap add ios
  npx cap add electron

Follow the Developer Workflow guide to get building:
https://capacitor.ionicframework.com/docs/basics/workflow

$ yarn build
$ yarn add cross-env
$ npx cap add android
$ npx cap add ios # Errorが出た https://qiita.com/macococo/items/41a1ea97ddd9f6974032 の sudo xcode-select -r を実行したら、無事に実行できた
$ npx cap add electron

$ yarn build
$ npx cap copy # 全プラットホームを更新
$ npx cap open android # Android Studioが開く
$ npx cap open ios # XCodeを開く
```

下記の記事を参考にさせていただいた

https://www.smashingmagazine.com/2018/07/mobile-apps-capacitor-vue-js/

## Capacitor For Web Startup

このプロジェクトをCapacitorのWebで起動する方法

```sh
$ yarn build
$ npx cap copy web
$ sudo npx cap serve
```

下記の公式を参考にした

https://capacitor.ionicframework.com/docs/web

## Capacitor For Electron setup

このプロジェクトをCapacitorのElectronで起動する方法

```sh
$ yarn build:electron
$ npx cap add electron # 初回のみ
$ npx cap copy electron
$ npx cap open electron
```

下記の公式を参考にした

https://capacitor.ionicframework.com/docs/electron

## Build Setup

``` bash
# install dependencies
$ yarn install

# serve with hot reload at localhost:3000
$ yarn dev

# build for production and launch server
$ yarn build
$ yarn start

# generate static project
$ yarn generate
```

For detailed explanation on how things work, check out [Nuxt.js docs](https://nuxtjs.org).
