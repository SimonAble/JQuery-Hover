# JQuery-Hover
This is a simple implementation of the .hover JQuery Function. Visit the page <a href="https://simonable.github.io/JQuery-Hover/"> Here </a>

##The function works by changing two aspects of the html when the mouse hovers over it. 

1. It changes the attr containing the image, changing it to another image.
2. It also adds a class to the image, giving it the 'glowing effect' created by adding a box shadow.

```javascript
  $( "#switch" ).hover(
    function() {
        $(this).addClass( "hover" );
        $(this).attr("src", "img/switch2.jpg"); 

    }, function() {
        $( this ).removeClass( "hover" );
        $(this).attr("src", "img/switch1.png"); 
    }
);
```

##The html uses an alternate data source to store the second image value. When the function is called it knows to make the secondary source the new img src.

```html
  <!--Switch-->
    <div class="container">
       <img id="switch" src="img/switch1.png" data-alt-src="img/switch2.jpg">
    </div>
```


![](https://github.com/SimonAble/JQuery-Hover/blob/master/img/Hover1.png)

![](https://github.com/SimonAble/JQuery-Hover/blob/master/img/Hover2.png)
