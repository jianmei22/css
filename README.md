小码农的css进阶学习
1、	清除浮动
html
<div class="clearfix">
  <div class="floated">float a</div>
  <div class="floated">float b</div>
  <div class="floated">float c</div>
</div>
css
.clearfix::after {
  content: '';
  display: block;
  clear: both;
}
.floated {
  float: left;
}
.clearfix::after定义伪元素
Content:””; 允许伪元素影响布局
Clear:both 清除所有浮动
2、	等宽高比（给定可变宽度的元素，它将确保其高度以响应的方式保持成比例（即，其高度和宽度的比率保持恒定）
Html
<div class="constant-width-to-height-ratio"></div>
Css
.constant-width-to-height-ratio {
  background: #333;
  width: 50%;
}
.constant-width-to-height-ratio::before {
  content: '';
  padding-top: 100%;
  float: left;
}
.constant-width-to-height-ratio::after {
  content: '';
  display: block;
  clear: both;
}
调整浏览器大小查看元素的比例保持不变
：：before伪元素使元素的高度等于其宽度的百分比
3、	均匀分布的子元素（在父元素中均匀分布的子元素）HTML
<div class="evenly-distributed-children">
  <p>Item1</p>
  <p>Item2</p>
  <p>Item3</p>
</div>
.evenly-distributed-children {
  display: flex;
  justify-content: space-between;}
display:flex;弹性盒子布局，是前端布局神器
详细讲解参考：https://www.cnblogs.com/qingchunshiguang/p/8011103.html
弹性盒子：flexible box，为盒装模型提供最大的灵活性，任何一个容器都可以指定为flex布局。
行内元素也可以使用flex布局：display:inline-flex;
兼容性写法：display：flex||inline-flex；
Flex容器结构示意图：
 
容器属性：

