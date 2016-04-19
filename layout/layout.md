# CSS布局实现（未完）
---
## 左侧定宽，右侧自适应宽度布局
最开始想到使用绝对定位position:absolute定位实现，但是由于脱离文档流导致页面高度不能自动撑开，所以选择使用浮动并且在外层清除浮动的做法。
基本思路：左侧div定宽float，右侧div宽度auto
#### HTML DOM如下
```
<div class="container">
	<div class="layout-left bg-red">
		<p>LEFT</p>
		<p>width:190px</p>
	</div>
	<div class="layout-right bg-blue">
		<p>RIGHT</p>
	</div>
</div>
```
#### [demo - columns2.html](columns2.html)
---
## 左右定宽，中间自适应宽度布局
#### [demo - columns3.html](columns3.html)
