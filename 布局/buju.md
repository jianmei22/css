##清除浮动
* html
'''
<div class="clearfix">
  <div class="floated">float a</div>
  <div class="floated">float b</div>
  <div class="floated">float c</div>
</div>
'''
*css
'''
.clearfix::after {
  content: '';
  display: block;
  clear: both;
}
.floated {
  float: left;
}
'''
![我是图片](https://github.com/jianmei22/css/blob/master/%E5%B8%83%E5%B1%80/flex.png)
