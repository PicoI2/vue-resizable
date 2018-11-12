# VueResizable

[![Latest Version on NPM](https://img.shields.io/npm/v/vue-resizable.svg?style=flat-square)](https://npmjs.com/package/vue-resizable)
[![npm](https://img.shields.io/npm/dt/vue-resizable.svg?style=flat-square)](https://www.npmjs.com/package/vue-resizable)
[![Software License](https://img.shields.io/badge/license-MIT-brightgreen.svg?style=flat-square)](LICENSE.md)

![](./docs/logo.gif) 

> Vue component that allows resizing elements

### Demo

[CodeSandbox](https://codesandbox.io/s/13qp7xk787)

## Installation

```sh
npm install vue-resizable --save
```

## Basic usage

```vue
<template>
    <vue-resizable>
        <div class="resizable-content"></div>
    </vue-resizable>
</template>

<script>
import VueResizable from 'vue-resizable'

export default {
    name: "YourApp",
    components: {VueResizable}
}
</script>

<style scoped>
    .resizable-content {
        height: 100%;
        width: 100%;
        background-color: aqua;
    }
</style>
```

## Properties


| Property            |  Data attribute    | Type    | Default | Description                                                                                                                                                                                                                                                                           |
|:--------------------|------|:--------|:--------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| width               |   w   | [Number, String] | 200   | Width           
| minWidth            |   minW   | Number  | 0    |  Minimal width     
| maxWidth            |   maxW    | Number | undefined   | Maximal width
| height               |  h   | [Number, String]  | 200    | Height                                                                                                                                                                                                                    |
| minHeight        | minH | Number  | 0       | Minimal height                                                                                                                                                                                                                |
| maxHeight    | maxH | Number  | undefined       | Maximal height                                                                                                                                                                                                                              |
| left          |   l    | [Number, String] | 0    | Offset left from parent                                                                                                                                                                                                                                                     |
| top       | t | [Number, String] | 0   | Offset top from parent          
| active     |    | Array | ['r', 'rb', 'b', 'lb', 'l', 'lt', 't', 'rt']   | Active handlers for resize    
| fitParent    |     | Boolean | false  | Respect parent's size on resizing

## Events

| Name            |  Payload   |  Description                                                                                                                                                                                                                                                                           |
|:--------------------|-------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| resize:mount               |   [left,top,width,height]      | Called after the component is mounted 
| resize:destroy               |   [left,top,width,height]      | Called before the component is destroyed 
| resize:start               |   [left,top,width,height]      | Called after clicking on one of the active handlers 
| resize:move               |   [left,top,width,height]      | Called when a handler is being dragged
| resize:end               |   [left,top,width,height]      | Called when the mouse button was released

## Development



To begin development, run:

``` bash
npm install 
npm run dev
```
It starts [webpack-dev-server](https://github.com/webpack/webpack-dev-server) on `localhost:8080` with [Demo](./docs) page.

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details.


     