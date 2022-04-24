# 基本组件实现思路：

1.  下拉框

<img src="https://raw.githubusercontent.com/HYHL0909/images/main/202204241120263.png" alt="image-20220424111940629" style="zoom:25%;" />



布局：

dropdown

`.dropdown` 类使用 `position:relative`, 这将设置下拉菜单的内容放置在下拉按钮 (使用 `position:absolute`) 的右下角位置。

block 变成inline-block ，如果不设置长度，则是根据子元素的内容宽度撑开

- dropdown-btn （button，span，a）

- dropdown-content  容器元素 

   如果你想设置下拉内容与下拉按钮的宽度一致，可设置 `width` 为 100% ( `overflow:auto` 设置可以在小尺寸屏幕上滚动)。

  我们使用 `box-shadow` 属性让下拉菜单看起来像一个"卡片"。

  - a
  - a
  - a

`:hover` 选择器用于在用户将鼠标移动到下拉按钮上时显示下拉菜单。



下拉框实例：

![image-20220325194942997](C:\Users\Elvira\AppData\Roaming\Typora\typora-user-images\image-20220325194942997.png)

![image-20220325205155973](C:\Users\Elvira\AppData\Roaming\Typora\typora-user-images\image-20220325205155973.png)



inline行内元素的特点

1. 行内元素不会独占一行，多个行内元素会排成一行，直到充满整行之后再换行。
2. 行内元素不能设置width和height属性
3. 设置margin和padding属性时，margin-top，margin-bottom，padding-top，padding-bottom无效。行内元素的padding-top和padding-bottom在浏览器中会显示出效果，但是并没有实际作用，对周围的元素没有影响。

block 变成inline-block ，如果不设置长度，则是根据子元素的内容宽度撑开。
