### CSS网页布局

![image-20220326172845660](C:\Users\Elvira\AppData\Roaming\Typora\typora-user-images\image-20220326172845660.png)

![image-20220326172910975](C:\Users\Elvira\AppData\Roaming\Typora\typora-user-images\image-20220326172910975.png)

当屏幕尺寸小于800px时，两列布局改为上下布局。



containner

- header

- topnav

  overflow：hidden

  因为float 所以塌陷

- row
  - left
    - card
    - card
  - right
    - card
    - card

- row后面清除浮动
  
- footer

 @media screen and (max-width:800px) {

​    .right,.left,.topnav a{

​      width:100%;

​    }