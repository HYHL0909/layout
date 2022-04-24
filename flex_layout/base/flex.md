如果是pc端页面布局，传统布局
移动端或者不考虑兼容性问题的pc端页面布局，选择flex
布局原理：弹性布局=伸缩布局=伸缩盒布局=弹性盒布局=flex布局。
通过给父盒子添加flex属性，来控制子盒子的的位置盒排列方式。
任何容器（块、行）都是可以指定为flex属性。
**当父盒子设定为flex布局之后**，**子元素的float、clear和vertical-align属性将失效。**
flex父容器，项目（第一级子元素）

# 父项常见属性
flex-direction:主轴方向，默认水平向右；侧轴默认向下。row|col
主轴：
子元素上排列方式：

**justify-content** ：flex-start|flex-end|center|space-around|space-between（重要）

**flex-wrap**：nowrap(default)|wap 设置子元素是否换行
默认是不换行的，项目都排在一条线上，如果塞不进去就缩小子元素大小。

**align-items**(单行):flex-start(default)|flex-end|center|strentch

想要垂直居中又想水平居中，如果只是有justify-content，那么尽管换了轴，也只能实现贴边居中。

align-content ：flex-start|flex-end|center|space-around|space-between|strentch
只有在子元素出现换行（！！）的情况下才有用。单行下是没有效果的。


flex-flow  把设置主轴和是否换行简写
flex-flow：column wrap；

# 子项常见属性
flex：0（default）
定义子项目   分配剩余空间(!!)。用flex表示占多少份数。
**左侧固定，右侧固定，中间独占所有站一份**

~~~html
 <div id="div0">
        <div>1</div>
        <div>2</div>
        <div>3</div>
 </div>
<style>
        #div0{
            display:flex ;
        }
        #div0 div:first-child{
            flex:0 0 50px;
        }
        #div0 div:nth-child(2){
            flex:1 1 auto;
        }

        #div0 div:last-child{
            flex:0 0 50px;
        }
</style>


~~~



align-self：控制子项自己在侧轴上的排列方式 那么父容器之中align-items属性可以被覆盖
order 定义子项目顺序。默认是0.比较小的在前面。



局部自适应

左边和右边固定，中间随着屏幕size的增大而进行增大，减小而减小

利用flex 和媒体查询


# 携程网案例学习

整体布局

![image-20220423193803019](https://raw.githubusercontent.com/HYHL0909/images/main/202204232048973.png)

![image-20220423193825674](https://raw.githubusercontent.com/HYHL0909/images/main/202204232048900.png)



box-sizing:

border-box ： 为元素设定的宽度和高度决定了元素的边框盒。

content-box：默认，宽度和高度分别应用到元素的内容框



手机布局

body max-width



div .search-index

固定：fixed 宽度自定义，与父级的宽度没有关系，虽然body已经定义了width

居中 ：兼容的

flex

- 布局

  - 伪元素实现 搜索号

  - div search

    居中  lineheight  height  

    position ：relative

    padding-left：给伪元素留位置

    伪元素实现 

    .search ::before{

    position ：absolute

    background：url（） no-repeat 

    }

    - span

  - a  user

    使用伪元素从精灵图里抠出来

div .focus

- img  width：100%



ul .local-nav

display：flex

- li

  flex：1

  - a

    display：flex

    - span
    - span



nav

![image-20220423204807797](https://raw.githubusercontent.com/HYHL0909/images/main/202204232048721.png)

- nav-common
  
  display：flex
  
  /*第一个nav-item的a*/  ` .nav-items:nth-child(1) a`
  
  /*mav-item的第一个a*/ `.nav-items a:nth-child(1)`
  
  /*选择后面两个元素*/  ` .nav-items:nth-child(n+2)`
  
  - nav-items
    
    颜色渐变：记得加上浏览器前缀
    
      background:-webkit-linear-gradient(left,#4B8FED,#53BCED);
    
    flex：1
    
    边界线通过元素选择，用border 做的
    
    - a #logo1
    
  - nav-items
  
    - a 
    - a 
  
- nav-common
  - nav-items
    - a #logo1
  
- nav-common
  - nav-items
    - a #logo1



![image-20220423205543675](C:/Users/Elvira/AppData/Roaming/Typora/typora-user-images/image-20220423205543675.png)



ul .subnav-entry

  弹性布局，有分行，display: flex;  flex-wrap: wrap;

- li

  flex：20%

  - a

    flex

    方向变成垂直： flex-direction

    - span
    - span



div .sales-box

- sales-hd
  - h2
  - a
- sales-bd
  - row
  - row

ul .footer

display: flex

- li

  flex：1

  - a

    display：flex

    flex-direction：column

    - span

    - span

      

div .liscence

居中

- nav-row

  display：flex

  - span
  - span
  - span

- nav-row

  - span
  - span
