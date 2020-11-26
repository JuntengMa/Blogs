---
layout: 
title: 自定义webpack配置
date: 2020-11-23 15:29:16
tags:
---

# create-react-app 自定义配置webpack

<!-- more -->

#### 1、修改webpack配置文件，需要安装 react-app-rewired customize-cra

```
yarn add react-app-rewired customize-cra -D
```

#### 2、修改package.json文件

```
"scripts": {
    "start": "react-app-rewired start",
    "build": "react-app-rewired build",
    "test": "react-app-rewired test --env=jsdom",
    "eject": "react-scripts eject"
  },
```

#### 3、在项目根目录新建config-overrides.js

```
const { override } = require('customize-cra');
module.exports = {};
```