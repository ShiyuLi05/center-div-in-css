# Center div in CSS
A few ways to center div in CSS

## ```div``` and CSS
The tag ```<div>``` defines a division or a section in an HTML document.

The tag ```<div>``` is used as a container for HTML elements - which is then styled with CSS or manipulated with JavaScript.

The tag ```<div>``` is easily styled by using the class or id attribute.

CSS is the language we use to style an HTML document.
CSS describes how HTML elements should be displayed.

This tutorial will teach you how to center a div using CSS.


### I. Using margin

To center the div horizontally, set the left and right margins to ```auto```.

To center the div vertically, calculate the top and bottom margins,
which are half the height of the parent container minus half the height of the child container.

```HTML
<!DOCTYPE html> 
<html lang ="en" dir="ltr">
    <head>
        <meta charset="utf-8"> 
        <meta name="viewport"content="width=device-wode,initial-scale=1">
        <meta name="author"content="Shiyu Li">
        <meta name="description"content="My web page">
        <meta name="keywords"content="html,css,web,web developmet,seo">
        <title>Center a div</title>
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
        </style>
    </head>
    <body>
        <div class="container">
            <div class="child"></div>
        </div>
    </body>
</html> 
```


### II. absolute position
make the child container is enable with ```position: absolute```; and make sure left, right, top and bottome are all 0;  ```margin :auto```
```HTML
        <style>
            *{
                margin: 0;
                padding: 0;
            }
            .container {
                height: 800px;
                background-color: #000;
                position: relative;
            }
            .child {
                width: 300px;
                height: 300px;
                background-color: #fff;
                position: absolute;
                left: 0;
                right: 0;
                top: 0;
                bottom: 0;
                margin: auto;
            }
        </style>
```

### III. relative position
Relative positioning for the parent container and absolute positioning for child container. 
```HTML
        <style>
            *{
                margin: 0;
                padding: 0;
            }
            .container {
                height: 800px;
                background-color: #000;
                position: relative;
            }
            .child {
                width: 300px;
                height: 300px;
                background-color: #fff;
                position: absolute;
                top: 50%;
                margin-top: -150px;
                left: 50%;
                margin-left: -150px;
            }
        </style>
```

### IV. flex layout
```HTML
      <style>
            *{
                margin: 0;
                padding: 0;
            }
            .container {
                height: 800px;
                background-color: #000;
                display: flex;
                justify-content: center;
                align-items: center;
            }
            .child {
                width: 300px;
                height: 300px;
                background-color: #fff;
            }
        </style>
```
![image](https://github.com/ShiyuLi05/center-div-in-css/blob/main/center%20div.png)
