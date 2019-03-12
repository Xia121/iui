# IUI - 一个Vue UI 组件[![Build Status](https://travis-ci.org/travis-ci/docs-travis-ci-com.svg?branch=master)](https://travis-ci.org/travis-ci/docs-travis-ci-com)

## 介绍

这是我在学习 Vue 过程中做的一个 UI 框架，希望对你有用

## 开始使用

1. 添加 CSS 样式

    使用本框架前， 请在 CSS 中开启 border-box
    
    *,*::before,*::after{box-sizing: border-box;}
    
    你还需要设置默认颜色 后续会改成 SCSS 变量
    
    IE 8 及以上的浏览器支持此样式。
    
    :root {
        --button-height: 32px;
        --font-size: 14px;
        --button-bg: white;
        --button-active-bg: #eee;
        --button-radius: 4px;
        --color: #333;
        --border-color: #999;
        --border-color-hover: #666;
    }
            
    IE 15 及以上的浏览器支持此样式。
    
2. 安装 IUI 
    npm i --save IUI
    
3. 引入 IUI

    import Button from './button'
    import Icon  from './icon'
    import ButtonGroup  from './button-group.vue'
    console.log(Button);
    Vue.component('g-button', Button)
    Vue.component('g-icon', Icon)
    Vue.component('g-button-group', ButtonGroup)
   
4. 引入 svg symbols

    <script src="//at.alicdn.com/t/font_1039312_paai4vxfrwh.js"></script> 
    
## 文档

## 提问

## 变更记录

## 联系方式 

## 贡献代码