# Notebook
## swiper实现不定高滑动效果
---
#### HTML DOM如下
```
<div class="swiper-container" id="swiper-container">
	<div class="swiper-wrapper">
		<div class="swiper-slide slide-1">slider1</div>
		<div class="swiper-slide slide-2">slider2</div>
		<div class="swiper-slide slide-3">slider3</div>
	</div>
</div>
```
#### 初始化swiper将slidesPerView属性设置为'auto'
```
var mySwiper = new Swiper('.swiper-container',{
  direction : 'vertical',
  slidesPerView : 'auto'
});
```
* 由于高度或宽度不再相同，swiper无法通过总高度得出参与loop的slide个数，所以loop模式下还需要设置另外一个参数loopedSlides，以告知swiper当前loop由多少slide构成。
####设定.swiper-container标签的高度
```
.swiper-container {
  height: 667px;
}
```
####设定每个滑动元素的高度
```
.slide-1 {
  height: 667px;
}
.slide-2 {
  height: 300px;
}
.slide-3 {
  height: 1200px;
}
```
---
* 一屏高度的slide-1将正常滚动
* 不足一屏的slide-2将滚动半屏(slide-2的高度)
* 大于一屏的slide-3将被分为多屏滚动
