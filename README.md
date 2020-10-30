# craco
[![NPM Status](https://img.shields.io/npm/v/@craco/craco.svg)](https://www.npmjs.com/package/@craco/craco)
[![Build Status](https://img.shields.io/travis/gsoft-inc/craco/master.svg?style=flat&label=travis)](https://travis-ci.org/gsoft-inc/craco)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-green.svg)](https://github.com/sharegate/craco/pulls)

[![NPM Downloads](https://img.shields.io/npm/dm/@craco/craco.svg)](https://www.npmjs.com/package/@craco/craco)

**C**reate **R**eact **A**pp **C**onfiguration **O**verride is an easy and comprehensible configuration layer for create-react-app.

Get all the benefits of create-react-app **and** customization without using 'eject' by adding a single `craco.config.js` file at the root of your application and customize your eslint, babel, postcss configurations and many more.

All you have to do is create your app using [create-react-app](https://github.com/facebook/create-react-app/) and customize the configuration with a `craco.config.js` file.

## Support

- Create React App (CRA) 3.*
- Yarn
- Yarn Workspace
- NPM
- Lerna (with or without hoisting)
- Custom `react-scripts` version

## Documentation
- [Preface](https://github.com/sharegate/craco/blob/master/packages/craco/README.md#preface)
- [Installation](https://github.com/sharegate/craco/blob/master/packages/craco/README.md#installation)
- [CRACO Configuration](https://github.com/sharegate/craco/blob/master/packages/craco/README.md#craco-configuration)
  - [The Mode Property](https://github.com/sharegate/craco/blob/master/packages/craco/README.md#the-mode-property)
  - [Sample CRACO Configuration File](https://github.com/sharegate/craco/blob/master/packages/craco/README.md#sample-craco-configuration-file)
  - [Setting a Custom Location for `craco.config.js`](https://github.com/sharegate/craco/blob/master/packages/craco/README.md#setting-a-custom-location-for-cracoconfigjs)
  - [`when` Shortcuts](https://github.com/sharegate/craco/blob/master/packages/craco/README.md#when-shortcuts)
- [Extra Help for React and Webpack Toolchain Beginners](https://github.com/sharegate/craco/blob/master/packages/craco/README.md#extra-help-for-react-and-webpack-toolchain-beginners)
  - [Notes on CRA Configurations and Problem Solving](https://github.com/sharegate/craco/blob/master/packages/craco/README.md#notes-on-cra-configurations-and-problem-solving)
  - [Ejecting CRA to Learn](https://github.com/sharegate/craco/blob/master/packages/craco/README.md#ejecting-cra-to-learn)
  - [Direct Versus Functional Config Definitions](https://github.com/sharegate/craco/blob/master/packages/craco/README.md#direct-object-literal-versus-functional-config-definitions)
- [CRACO API](https://github.com/sharegate/craco/blob/master/packages/craco/README.md#craco-api) - Access CRACO-generated configurations for Jest and Webpack
  - [Jest Config Generation](https://github.com/sharegate/craco/blob/master/packages/craco/README.md#jest-config-generation)
  - [Webpack DevServer and Production Config Generation](https://github.com/sharegate/craco/blob/master/packages/craco/README.md#webpack-devserver-and-production-config-generation)
- [Recipes](https://github.com/sharegate/craco/blob/master/packages/craco/README.md#recipes)
- [Plugins](https://github.com/sharegate/craco/blob/master/packages/craco/README.md#plugins)
  - [Available Plugins](#community-maintained-plugins)
  - [Developing a New Plugin](https://github.com/sharegate/craco/blob/master/packages/craco/README.md#developing-a-new-plugin) - How to develop a plugin for CRACO.
    - [Plugin Functions](https://github.com/sharegate/craco/blob/master/packages/craco/README.md#plugin-functions)
    - [Utility Functions for Development](https://github.com/sharegate/craco/blob/master/packages/craco/README.md#utility-functions-for-development)

## Community Maintained Plugins

* [craco-preact](https://github.com/FormAPI/craco-preact) by [@FormAPI](https://github.com/FormAPI)
* [craco-less](https://github.com/FormAPI/craco-less) by [@FormAPI](https://github.com/FormAPI)
* [craco-antd](https://github.com/FormAPI/craco-antd) by [@FormAPI](https://github.com/FormAPI)
* [craco-plugin-react-hot-reload](https://github.com/HasanAyan/craco-plugin-react-hot-reload) by [@HasanAyan](https://github.com/HasanAyan)
* [craco-babel-loader](https://github.com/rjerue/craco-babel-loader) by [@rjerue](https://github.com/rjerue/)
* [craco-raw-loader](https://github.com/melMass/craco-raw-loader) by [@melMass](https://github.com/melMass)
* [craco-base64-inline-loader](https://github.com/melMass/craco-base64-inline-loader) by [@melMass](https://github.com/melMass)
* [craco-workbox](https://github.com/kevinsperrine/craco-workbox) by [@kevinsperrine](https://github.com/kevinsperrine)
* [craco-use-babelrc](https://github.com/jackwilsdon/craco-use-babelrc) by [@jackwilsdon](https://github.com/jackwilsdon)
* [craco-image-optimizer-plugin](https://github.com/kkulbae/craco-image-optimizer-plugin) by [@kkulbae](https://github.com/kkulbae)
* [craco-interpolate-html-plugin](https://github.com/kkulbae/craco-interpolate-html-plugin) by [@kkulbae](https://github.com/kkulbae)
* [craco-cesium](https://www.npmjs.com/package/craco-cesium) by [rot1024](https://github.com/rot1024)
* [craco-sass-resources-loader](https://github.com/tilap/craco-sass-resources-loader) by [tilap](https://github.com/tilap)
* [craco-linaria](https://github.com/jedmao/craco-linaria) by [jedmao](https://github.com/jedmao)
* [craco-plugin-scoped-css](https://github.com/gaoxiaoliangz/react-scoped-css/tree/master/packages/craco-plugin-scoped-css) by [gaoxiaoliangz](https://github.com/gaoxiaoliangz)
* [craco-alias](https://github.com/risenforces/craco-alias) by [@risenforces](https://github.com/risenforces)
* [craco-favicons](https://github.com/rickysullivan/craco-favicons) by [@rickysullivan](https://github.com/rickysullivan)
* [craco-styled-jsx](https://github.com/cr4zyc4t/craco-styled-jsx) by [@cr4zyc4t](https://github.com/cr4zyc4t)
* [craco-purescript-loader](https://github.com/andys8/craco-purescript-loader) by [@andys8](https://github.com/andys8)
* [craco-fast-refresh](https://github.com/vimcaw/craco-fast-refresh) by [@vimcaw](https://github.com/vimcaw)

## Acknowledgements

[@timarney](https://github.com/timarney) for having created [react-app-rewired](https://github.com/timarney/react-app-rewired).

## License

Copyright © 2020, GSoft inc. This code is licensed under the Apache License, Version 2.0. You may obtain a copy of this license at https://github.com/gsoft-inc/gsoft-license/blob/master/LICENSE.
