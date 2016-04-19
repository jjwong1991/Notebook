# CSS布局实现（未完）
---
## 左侧定宽，右侧自适应宽度布局
最开始想到使用绝对定位position:absolute实现，但是由于完全脱离文档流导致页面高度不能自动撑开，所以选择使用浮动和margin-left来实现,并且在最外层清除浮动。
基本思路：左侧div定宽float，右侧div为默认block元素，宽度auto占满剩余区域。
#### HTML DOM如下
```
<div class="container">
	<div class="layout-left">
		<p>LEFT</p>
		<p>width:190px</p>
	</div>
	<div class="layout-right">
		<p>RIGHT</p>
	</div>
</div>
```
#### layout实现的CSS
###### 方法1
```
.container {
	margin-left: 190px;
}
.layout-left {
	float: left;
	width: 190px;
	height: 400px;
	margin-left: -190px;
}
.layout-right {
	height: 300px;
}
```
###### 方法2
```
/*.layout-left {
	float: left;
	width: 190px;
	height: 400px;
}
.layout-right {
	height: 300px;
	margin-left: 190px;
}*/
```
#### [demo - columns2.html](columns2.html)
---
## 左右定宽，中间自适应宽度布局
#### [demo - columns3.html](columns3.html)
