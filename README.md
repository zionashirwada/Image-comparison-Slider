# Awesome Image Comparison Slider using HTML CSS & JavaScript

A handy draggable slider or image comparison slider to quickly compare two images, powered by CSS3 and JavaScript/jQuery. In this program [Image Comparison Slider], there are two same images with different filters – black & white and colorized, and at first, both of these images are shown 50% of their total width as you can see in the image. At the center, there is a draggable slider to compare two images.

## [See The Sample WebPage](https://jsitor.com/h2e4TfLhf)
![Sample Gif](https://lh3.googleusercontent.com/dd8F8-6DTMw6bHKuUcDc3kNuDFbBa8MjGeGkwff6SehfLy2o_KOsgjJd6tNchw7gSsNc4s9NS2cGft0hKX-feMoh_26Cbqr97DhAR7CceyA5b8qo_BPSGCiHXInArC5n8OXDXf49=w2400)


If you’re a beginner and you know basic HTML & CSS, then you can also easily understand the codes behind creating this slider or you can also create this type of Image Comparison Slider. You may have seen this type of slider on many websites that are based on the jQuery plugin but it’s a pure JavaScript program.

# Image Comparison Slider [Source Codes]

To create this program (Image Comparison Slider). First, you need to create two Files one HTML File and another one is CSS File. After creating these files just paste the following codes in your file.

1.First, create an HTML file with the name of [index.html](https://github.com/zionashirwada/Image-comparison-Slider/blob/main/index.html) and paste the given codes in your HTML file. Remember, you’ve to create a file with .html extension and the images that are used on this Comparison Slider won’t appear. You’ve to download files 

```
<!DOCTYPE html>
<html lang="en" dir="ltr">
  <head>
    <meta charset="utf-8">
    <title>Image Comparison Slider | Zion Ashirwada</title>
    <link rel="stylesheet" href="style.css">
  </head>
  <body>
    <div class="wrapper">
      <div class="images">
        <div class="img-1"></div>
        <div class="img-2"></div>
      </div>
      <div class="slider">
        <div class="drag-line">
          <span></span>
        </div>
        <input type="range" min="0" max="100" value="50">
      </div>
    </div>
    <div class="copyright"> Coded by <a href="https://github.com/zionashirwada"> Zion Ashirwada </a></div>
    

    <script>
      const slider = document.querySelector(".slider input");
      const img = document.querySelector(".images .img-2");
      const dragLine = document.querySelector(".slider .drag-line");
      slider.oninput = ()=>{
        let sliderVal = slider.value;
        dragLine.style.left = sliderVal + "%";
        img.style.width = sliderVal + "%";
      }
    </script>

  </body>
</html>

```
2.Second, create a CSS file with the name of [style.css](https://github.com/zionashirwada/Image-comparison-Slider/blob/main/style.css) and paste the given codes in your CSS file. Remember, you’ve to create a file with .css extension.

```
*{
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
html,body{
  display: grid;
  height: 100%;
  place-items: center;
  background: #efefef;
}
.copyright{
  font-size: 150%;
}
.wrapper{
  position: relative;
  height: 500px;
  width: 750px;
  overflow: hidden;
  background: #fff;
  border: 7px solid #fff;
  box-shadow: 0px 0px 15px rgba(0,0,0,0.15);
}
.wrapper .images{
  height: 100%;
  width: 100%;
  display: flex;
}
.wrapper .images .img-1{
  height: 100%;
  width: 100%;
  background: url("images/img.jpg") no-repeat;
  /* background: url("images/car.jpg") no-repeat; */
}
.wrapper .images .img-2{
  position: absolute;
  height: 100%;
  width: 50%;
  /* filter: blur(5px); */
  background: url("images/img.png") no-repeat;
  /* background: url("images/car.png") no-repeat; */
}
.wrapper .slider{
  position: absolute;
  top: 0;
  width: 100%;
  z-index: 99;
}
.wrapper .slider input{
  width: 100%;
  outline: none;
  background: none;
  -webkit-appearance: none;
}
.slider input::-webkit-slider-thumb{
  height: 486px;
  width: 3px;
  background: none;
  -webkit-appearance: none;
  cursor: col-resize;
}
.slider .drag-line{
  width: 3px;
  height: 486px;
  position: absolute;
  left: 49.85%;
  pointer-events: none;
}
.slider .drag-line::before,
.slider .drag-line::after{
  position: absolute;
  content: "";
  width: 100%;
  height: 222px;
  background: #fff;
}
.slider .drag-line::before{
  top: 0;
}
.slider .drag-line::after{
  bottom: 0;
}
.slider .drag-line span{
  height: 42px;
  width: 42px;
  border: 3px solid #fff;
  position: absolute;
  top: 50%;
  left: 50%;
  border-radius: 50%;
  transform: translate(-50%, -50%);
}
.slider .drag-line span::before,
.slider .drag-line span::after{
  position: absolute;
  content: "";
  top: 50%;
  border: 10px solid transparent;
  border-bottom-width: 0px;
  border-right-width: 0px;
  transform: translate(-50%, -50%) rotate(45deg);
}
.slider .drag-line span::before{
  left: 40%;
  border-left-color: #fff;
}
.slider .drag-line span::after{
  left: 60%;
  border-top-color: #fff;
}

```

That’s all, now you’ve successfully created an Awesome Image Comparison Slider using HTML CSS & JavaScript. If your code doesn’t work or you’ve faced any error/problem then please download the source code files . It’s free and a .zip file will be downloaded then you’ve to extract it.


