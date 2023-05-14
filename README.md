# Center words in div
A few ways to center words in div

### I. Use line-height (for one line text)
```HTML
    <style>
        *{
            margin: 0;
            padding: 0;
        }
        .parent {
            height: 800px;
            background-color: #000;
            border: 1px solid;
        }
        .child {
            width: 300px;
            height: 300px;
            background-color: #fff;
            margin: 250px auto;
            font-size: 30px;
            line-height: 300px; /* Vertical center */
            text-align: center; /* Horizontal center */
        }
    </style>

<body>
    <div class="parent">
        <div class="child">
            Hello world.
        </div>
    </div>
</body>
```
![image](https://raw.githubusercontent.com/ShiyuLi05/center-div-in-css/main/center-words.png)

### I. Use line-height (for multi-line text)
a. the height of parent element is not-fixed
```HTML
<style>
    .child {
        width: 300px;
        background-color: #fff;
        margin: 250px auto;
        font-size: 30px;
        text-align: center;  /* Horizontal center */
        padding: 50px 20px; /* Vertical center */
    }
</style>

<div class="parent">
    <div class="child">
        Hello world.
        Hello world.
        Hello world.
        Hello world.
    </div>
</div>
```
![image](https://raw.githubusercontent.com/ShiyuLi05/center-div-in-css/center-words/center-words-2.png)

b.(i) the height of parent element is fixed
```HTML
<style>
    .child {
        display: table;
        width: 500px;
        height: 500px;
        font-size: 30px;
    }
    .child-middle {
        display: table-cell; 
        vertical-align: middle; /* Horizontal center */
        text-align: center; /* optional */
    }
</style>

<div class="parent">
    <div class="child">
        <div class="child-middle">
            IE6 & IE7 can't use this way.
            IE6 & IE7 can't use this way.
            IE6 & IE7 can't use this way.
            IE6 & IE7 can't use this way.
        </div>
    </div>
</div>
```
![image](https://raw.githubusercontent.com/ShiyuLi05/center-div-in-css/center-words/center-words-3.png)

` Some explanation about 'display:table' ` </br>
 (1) When use 'display:table', 'padding' can't work.</br>
 (2) When use 'display:table-row', 'padding' and 'margin' can't work.</br>
 (3) When use 'display:table-cell', 'margin' can't work.</br>
 </br>
 b.(ii) For IE7 and lower (fixed height)
 ```HTML
<style>
    .parent {
        position: relative;
        top: 0;
        left: 0;
        width: 400px;
        height: 400px;
        margin: 50px auto;
        border: 1px solid;
        background-color: #fff;
    }
    .child {
        width: 100%;
        text-align: center; /* Vertical center */
   /* - - - -Horizontal center - - -  */
        position: absolute; 
        top: 50%;
        left: 50%;
        transform: translate(-50%, -50%);
    }
</style>

<div class="parent">
    <div class="child">
        <div class="child-middle">
            fixed height can use with IE7
            fixed height can use with IE7
            fixed height can use with IE7
            fixed height can use with IE7
        </div>
    </div>
</div>
 ```
 ![image](https://raw.githubusercontent.com/ShiyuLi05/center-div-in-css/center-words/center-words-4.png)
```Some explanation about 'vertical-alian'```
(1) 'vertical-alian shoulde be used on 'inline' element include 'inline-block';</br>
(2) If the height of the text over than the height of container, 'vertical-alian: center' can't work;</br>
