
 # 响应式布局

两种主要的方式：

1. css3-media query：外联或内嵌。

   device-width，device-height--屏幕宽高

   width，height --渲染窗口宽高

   orientation --设备方向

   resolution --设备分辨率

   ~~~html
   <!--外联-->
   <html>
       <head>
           <link type="text/css" ref="stylesheet" href="link.css" media = "only screen and (max-width:480px)"/>
   
       </head>
   </html>
   ~~~

   ~~~html
   <!--内嵌-->
   <html>
       <head>       
           <style>
               @media screen and (min-width:480px){
                   
               }
           </style>
       </head>
   </html>
   ~~~

   

2. 利用一些框架。bootstrap

   Bootstrap提供了一套响应式、移动设备优先的流式栅格系统，随着屏幕或视口（viewport）尺寸的增加，系统会自动分为最多12列。

   使用Bootstrap响应式布局，

   首先需要在`head`中引入`meta`标签，添加`viewpirt`属性，`content`属性，其`content`中宽度等于设备宽度，

   ` initial-scale`:页面首次被显示可见区域的缩放级别，取值1则页面按实际尺寸显示，无任何缩放；

   ~~~html
   <head>
      <meta name="viewport" content="width=device-width, initial-scale=1"> 
        <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.1.3/dist/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-1BmE4kWBq78iYhFldvKuhfTAU6auU8tT94WrHftjDbrCEXSU1oBoqyl2QvZ6jIW3" crossorigin="anonymous">
   </head>
   
   ~~~

   

   栅格系统 Grid System

   按钮 Button

   组件：

   - page   

   

   