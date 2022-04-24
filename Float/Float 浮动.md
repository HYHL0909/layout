# Float 浮动

### Float 最初的功能：实现文字环绕。

### 清除浮动

浮动具有破坏性。因此要清除浮动。破坏性就是父容器变成一条线。

浮动让元素变成了block

- 在塌陷的父容器底部插入clear 

  会带来重叠效果bottom

  - 伪元素（推荐）

    - 只要应用在包含浮动子元素的父级元素上

      ~~~css
      .clearfix:after{
          content:"";
          display:table;
          clear:both;
      }
      ~~~

  - 在最后一个浮动标签后新加一个div标签，给其设置clear ：both

    

- 在父级元素添加overflow属性

  不会带来重叠效果。



### 浮动与流体布局。

![image-20220415164907449](https://raw.githubusercontent.com/HYHL0909/images/main/202204151649747.png)

![image-20220415164956771](https://raw.githubusercontent.com/HYHL0909/images/main/202204151649846.png)

  左边图片用width +float left

  右边是一个div 利用margin-left 写下左边图片

  的width。

  ![image-20220415165440406](https://raw.githubusercontent.com/HYHL0909/images/main/202204151654511.png)

- 方法实现一：改变DOM位置

  右边图片用width +float right

  左边是一个div 利用margin-right 写下右边图片的width。（但是这样改变了dom）的位置。

![image-20220415170519848](https://raw.githubusercontent.com/HYHL0909/images/main/202204151705915.png)

左边图片是float：left

右边div display：table-cell





元素的水平方向浮动，意味着元素只能左右移动而不能上下移动。

直到它的外边缘碰到包含框或另一个浮动框的边框为止。

浮动元素之后的元素将围绕它。如果不想让这个之后的元素围绕，可以清除浮动。

浮动元素之前的元素将不会受到影响。

```css
float:right|left
```

~~~html
<div>
    我是浮动的
</div>
<div>
    我是浮动的
</div>
<p>
    我不想浮动
</p>
<div>
    我是浮动的
</div>
<div>
    我是浮动的
</div>

<style>
    div{
        float:right;
        background-color:tan;
    }
    p{
        clear:both;
    }
</style>
~~~



比如p元素上面浮动

p元素下面的元素也浮动

但是中间元素不想浮动

利用浮动制作一个没有表格的网页。效果如下：

![](C:\Users\Elvira\AppData\Roaming\Typora\typora-user-images\image-20220325105059400.png)

布局：

![image-20220325121403880](C:\Users\Elvira\AppData\Roaming\Typora\typora-user-images\image-20220325121403880.png)



