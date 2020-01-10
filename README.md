# 仿zfb年度账单
## 配置相关

### 结合lib-flexible、px2rem实现移动端适配
* 项目中安装lib-flexible
* flexible会为页面根据屏幕自动添加<meta name='viewport' >标签，动态控制initial-scale，maximum-scale，minimum-scale等属性的值。
```HTML
npm install lib-flexible --save
``` 

* 在项目的入口main.js文件中引入lib-flexible
```HTML
import 'lib-flexible'
```

* 项目中安装postcss-px2rem-exclude
* postcss-px2rem-exclude会将px自动转换为rem，rem单位用于适配不同宽度的屏幕，根据<html>标签的font-size值来计算出结果，1rem=html标签的font-size值。
* 不使用postcss-px2rem；原因：第三库 css一依据 data-dpr=“1” 时写的尺寸，postcss-px2rem会根据动态data-dpr将第三方库内样式也转换为rem，造成页面样式问题。
```HTML
npm  install postcss-px2rem-exclude --save
```

* 配置exclude选项
* 配置位置--项目根目录下的postcss.config.js文件
```HTML
postcss.config.js

module.exports = {
  plugins: {
    autoprefixer: {},
    "postcss-px2rem-exclude": {
      remUnit: 75,
      exclude: /node_modules|folder_name/i
    }
  }
};
```

```HTML
package.json

"postcss": {
  "plugins": {
    "autoprefixer": {},
    "postcss-px2rem-exclude":{
        "remUnit": 75,
        "exclude":"/node_modules|floder_name/i"
    }
  }
}
```
* remUnit配置项的数值根据设计图的宽度来定，例如设计度宽度为750px，此时remUnit值为75；
* 引用像mint-ui这样的第三方UI框架时， 因为第三方框架没有兼容px2rem ，将remUnit的值设置为设计图宽度（这里为750px）75的一半，即可以1:1还原mint-ui的组件，否则会样式会有变化，例如按钮会变小。


### 全屏滚动vue-awesome-swiper
* 项目中安装lib-flexible
```HTML
cnpm install vue-awesome-swiper --save
```

* 全局挂载
```HTML
import Vue from 'vue'
import VueAwesomeSwiper from 'vue-awesome-swiper'

// require styles
import 'swiper/dist/css/swiper.css'

Vue.use(VueAwesomeSwiper, /* { default global options } */)
```

* 组件挂载
```HTML
// require styles
import 'swiper/dist/css/swiper.css'

import { swiper, swiperSlide } from 'vue-awesome-swiper'

export default {
  components: {
    swiper,
    swiperSlide
  }
}
```
```HTML
<!-- The ref attr used to find the swiper instance -->
<template>
  <swiper :options="swiperOption" ref="mySwiper" @someSwiperEvent="callback">
    <!-- slides -->
    <swiper-slide>I'm Slide 1</swiper-slide>
    <swiper-slide>I'm Slide 2</swiper-slide>
    <swiper-slide>I'm Slide 3</swiper-slide>
    <swiper-slide>I'm Slide 4</swiper-slide>
    <swiper-slide>I'm Slide 5</swiper-slide>
    <swiper-slide>I'm Slide 6</swiper-slide>
    <swiper-slide>I'm Slide 7</swiper-slide>
    <!-- Optional controls -->
    <div class="swiper-pagination"  slot="pagination"></div>
    <div class="swiper-button-prev" slot="button-prev"></div>
    <div class="swiper-button-next" slot="button-next"></div>
    <div class="swiper-scrollbar"   slot="scrollbar"></div>
  </swiper>
</template>

<script>
  export default {
    name: 'carrousel',
    data() {
      return {
        swiperOption: {
          // some swiper options/callbacks
          // 所有的参数同 swiper 官方 api 参数
          // ...
        }
      }
    },
    computed: {
      swiper() {
        return this.$refs.mySwiper.swiper
      }
    },
    mounted() {
      // current swiper instance
      // 然后你就可以使用当前上下文内的swiper对象去做你想做的事了
      console.log('this is current swiper instance object', this.swiper)
      this.swiper.slideTo(3, 1000, false)
    }
  }
</script>
```


### 简单动画效果animate.css
* 项目中安装animate.css
```HTML
npm install animate.css --save
``` 

* 在项目的入口main.js文件中引入animate.css
```HTML
import animated from 'animate.css'

Vue.use(animated)
```

* 在vuex项目中使用
* 直接使用animated中的动画class名，注意：必须使用animated这个class名，否则动画会无效
* flipInX效果为'水平翻转进入'
```HTML
<div class="text-detail-box text-detail-box-01" :class="thisActiveIndex == 1 ? 'animated flipInX' : ''">
  <p class="font-important-color">2019年</p>
  <p class="font-title-color">你更爱买化妆品类</p>
  <p class="font-title-color">商品共花费100万元</p>
  <p class="font-title-color">用剁手来表达爱</p>
</div>
```



