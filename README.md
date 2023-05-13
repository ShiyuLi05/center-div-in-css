# Center words in div
A few ways to center words in div

### I. Use line-height (for one line text)
```HTML
    <style>
        *{
            margin: 0;
            padding: 0;
        }
        .container {
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
    <div class="container">
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

<body>
<div class="container">
    <div class="child">
        Hello world.
        Hello world.
        Hello world.
        Hello world.
    </div>
</div>
</body>
```
![image](https://raw.githubusercontent.com/ShiyuLi05/center-div-in-css/main/center-words.png)

