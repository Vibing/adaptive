# adaptive.js
  - 借鉴手淘方案，使移动端自适应开发更方便。
  - 抛弃`[data-dpr="2"] span{font-size: 32px;}`的兼容写法
#

# theory
借鉴手淘方案，`adaptive.js`将整个页面宽度平均分成10份，以`clineWidth / 10`的结果作为`html`标签的`font-size`值。
布局中使用`rem`作为单位。举例：某UI设计出来的手机页面宽为`750px`，那么分成十份后为`75px`，此时`html`标签的`font-size: 75px`,
布局时某一模块在设计稿上宽为`100px`，转成`rem`则为：`100 / 75 = 1.3333rem`;在css中则为：`width: 1.3333rem`。

# usage
`adaptive.js`非常小巧,压缩后的`adaptive.min.js`大小只有1KB。
`adaptive.js`不依赖任何js库，你可以在head标签内引用`adaptive.min.js`后即可直接使用

# template
    <!DOCTYPE html>
    <html lang="en">
    <head>
        <meta charset="UTF-8">
        <meta name="viewport" content="initial-scale=1, maximum-scale=1,minimum-scale=1, user-scalable=no, minimal-ui">
        <meta name="apple-mobile-web-app-capable" content="yes">
        <meta name="apple-mobile-web-app-status-bar-style" content="black">
        <title>template</title>
        <script src="adaptive.min.js"></script>
        <style>
            .wrap{
                position: relative;
                width: 10rem;
                margin:0 auto;
            }
        </style>
        </head>
    <body>
    <div class="wrap">

    </div>
    </body>
    </html>

# demo
[点我查看小demo](https://vibing.github.io/adaptive)
你可以在任何安卓机或iphone上进行测试，如果有问题请到我的[segmentfault](https://segmentfault.com/u/ve)联系我
