# react-app-rewire-hot-loader-for-customize-cra
This project is a tiny wrapper of [react-app-rewire-hot-loader](https://github.com/cdharris/react-app-rewire-hot-loader), which aims to format it as a plugin of [customize-cra](https://github.com/arackaf/customize-cra).

基于 [react-app-rewire-hot-loader](https://github.com/cdharris/react-app-rewire-hot-loader) 封装，可以直接用于 [customize-cra](https://github.com/arackaf/customize-cra) 的插件
## Installation
```sh
yarn add -D 
react-app-rewire-hot-loader-for-customize-cra

# If you don't already, you also need:
yarn add -D react-app-rewired
yarn add -D react-hot-loader
yarn add -D customize-cra
```

## Usage
1. In the `config-overrides.js` of the root of your project you created for `react-app-rewired` add this code:

```js
const rewireReactHotLoader = require('react-app-rewire-hot-loader-for-customize-cra')
const { override } = require('customize-cra')

/* config-overrides.js */
module.exports = override(
  // ...other rewires
  rewireReactHotLoader()
)
```
2. Follow the rest guides: https://github.com/cdharris/react-app-rewire-hot-loader/blob/master/README.md#usage

## LICENSE 
MIT