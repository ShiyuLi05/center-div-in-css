# Center words in div
A few ways to center words in div

### I. Use line-height
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
        }
        p {
            line-height: 300px;
            text-align: center;
            font-size: 30px;
        }
    </style>

<body>
    <div class="container">
        <div class="child">
            <p>Hello world</p>
        </div>
    </div>
</body>
```
![image](https://raw.githubusercontent.com/ShiyuLi05/center-div-in-css/main/center-words.png)

