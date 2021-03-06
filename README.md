[![npm](https://img.shields.io/npm/l/vue-swiper.svg?maxAge=2592000)](https://raw.githubusercontent.com/weilao/vue-swiper/master/LICENSE)
[![npm](https://img.shields.io/npm/v/vue-swiper.svg?maxAge=2592000)](https://www.npmjs.com/package/vue-swiper)
[![GitHub release](https://img.shields.io/github/release/weilao/vue-swiper.svg?maxAge=2592000)](https://github.com/weilao/vue-swiper/releases)
[![GitHub issues](https://img.shields.io/github/issues/weilao/vue-swiper.svg?maxAge=2592000)](https://github.com/weilao/vue-swiper/issues)
[![GitHub stars](https://img.shields.io/github/stars/weilao/vue-swiper.svg?style=social&label=Star&maxAge=2592000)](https://github.com/weilao/vue-swiper) 

[![NPM](https://nodei.co/npm/vue-swiper.png?downloads=true&downloadRank=true)](https://nodei.co/npm/vue-swiper/)

# vue-swiper
Swiper component. Easy to use.

## Examples
[basic demo](http://weilao.github.io/vue-swiper/demo)

[webpack ES2015 demo](http://www.webpackbin.com/4kbKGs97b)

## Install
```
npm i vue-swiper -S
```

## Usage

```js
import Vue from 'vue'
import Swiper from 'vue-swiper'

new Vue({
    el: 'body',
    components: {Swiper},
    methods: {
        onSlideChangeStart (currentPage) {
            console.log('onSlideChangeStart', currentPage);
        },
        onSlideChangeEnd (currentPage) {
            console.log('onSlideChangeEnd', currentPage);
        }
    }
});
```

```html
<swiper v-ref:swiper
        direction="horizontal"
        :mousewheel-control="true"
        :performance-mode="false"
        @slide-change-start="onSlideChangeStart"
        @slide-change-end="onSlideChangeEnd">
    <div>Page 1</div>
    <div>Page 2</div>
    <div>Page 3</div>
</swiper>
```

## Api
### Properties

#### direction `String`	
Could be 'horizontal' or 'vertical' (for vertical slider). Defaults to `“vertical”`.

#### mousewheel-control `Boolean`	
Set to true to enable navigation through slides using mouse wheel. Defaults to `true`.

#### performace-mode `Boolean`
Disable advance effect for better performance. Defaults to `false`.

### Methods
#### next()
Go next page.

#### prev()
Go previous page.

#### setPage(`Number`)
Set current page number.

### Events
#### slide-change-start
Fire in the beginning of animation to other slide (next or previous).
 
#### slide-change-end
Will be fired after animation to other slide (next or previous).
