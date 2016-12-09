# adaptive.js
  - 修改手淘方案`flexible.js`，不再根据`dpr`的多少来缩放，使移动端自适应开发更方便。
  - 抛弃`[data-dpr="2"] span{font-size: 32px;}`的兼容写法
# 

# use
`adaptive.js`非常小巧,请在head标签内引用`adaptive.js`

# template
    <!DOCTYPE html>
    <html lang="en">
    <head>
        <meta charset="UTF-8">
        <meta name="viewport" content="initial-scale=1, maximum-scale=1,minimum-scale=1, user-scalable=no, minimal-ui">
        <meta name="apple-mobile-web-app-capable" content="yes">
        <meta name="apple-mobile-web-app-status-bar-style" content="black">
        <title>template</title>
        <script src="adaptive.js"></script>
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

# 说明
  - `adaptive.js`将屏幕宽度平均分成`10`份，`一份的宽度`即是`1rem`的值。例如：设计稿宽度为`750px`,分成`10`份后，每份宽度为`75px`,那么`1rem = 75px`。此时设计稿上有宽为`100px`的模块，换算成`rem`则是`100/75=1.3333rem`,体现在`css`上则是`width:1.3333rem`。
  - `adaptive.js`认为字体大小使用`rem`是件很糟糕的事，而是推荐使用`px`为单位。
  
# demo
[点我查看小demo](https://vibing.github.io/adaptive)
