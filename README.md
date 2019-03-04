小码农的css进阶学习
#清除浮动：
<div class="clearfix">
  <div class="floated">float a</div>
  <div class="floated">float b</div>
  <div class="floated">float c</div>
</div>
.clearfix::after {
  content: '';
  display: block;
  clear: both;
}
.floated {
  float: left;
  background-color: brown;
  margin-left: 20px;
}
