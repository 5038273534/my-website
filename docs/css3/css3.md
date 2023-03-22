```html
<!DOCTYPE html>
<html>

<head>

  <meta charset="UTF-8">
  <title>css text shadow</title>
  <meta name="viewport" content="width=device-width, initial-scale=1">
  
<style>

body {
  margin: 50px 50px;
  background: #fff;
  text-align: center;
}
div {
  margin:20px;
}
.demo {
      background: #666666;
      width: 440px;
      padding: 30px;
      font: bold 55px/100% "微软雅黑", "Lucida Grande", "Lucida Sans", Helvetica, Arial, Sans;;
      color: #fff;
      text-transform: uppercase;
}
.demo1 {
   text-shadow: red 0 1px 0;
}
.demo2 {
  text-shadow: 0 0 20px red;
}
.demo3 {
  text-shadow: 0 0 5px #fff, 0 0 10px #fff, 0 0 15px #fff, 0 0 40px #ff00de, 0 0 70px #ff00de;
}
.demo4 {
  color: #000;
  text-shadow: 0 1px 1px #fff;          
}
.demo5 {
  color: #ccc;
  text-shadow: -1px -1px 0 #fff,1px 1px 0 #333,1px 1px 0 #444;
}
.demo6 {
  color: transparent;
  text-shadow: 0 0 5px #f96;
}
.demo7 {
  color: transparent;
  text-shadow:0 0 6px #F96, -1px -1px  #FFF, 1px -1px  #444;
}
.demo8 {
  color: #566F89;
  background: #C5DFF8;
  text-shadow: 1px 1px 0 #E4F1FF;
}
.demo9 {
  color: #fff;
  text-shadow: 1px 1px 0 #f96,-1px -1px 0 #f96;
}
</style>

</head>

<body>

  <div class="demo demo1">text shadow</div>
  <div class="demo demo2">Glow and Extra Glow effect</div>
  <div class="demo demo3">NEON effect</div>
  <div class="demo demo4">Apple Style Effect</div>
  <div class="demo demo5">Photoshop Emboss Effect</div>
  <div class="demo demo6">Blurytext Effect</div>
  <div class="demo demo7">Emboss Effect</div>
  <div class="demo demo8">Inset Effect</div>
  <div class="demo demo9">Stroke Effect</div>


</body>

</html>

```


```css
box-sizing:border-box;


```