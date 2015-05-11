### jQuery插件jquery.boxhovermodal.js

	该插件是在鼠标滑过box的时候，通过鼠标进入的方向，使modal层从box上下左右不同的方向进入。

#### HTML部分

	一个class为box-hover-modal的块内部包含一个class为box-hover-modal-m的绝对定位块

```html
<div class="box-hover-modal">
	<div class="box-hover-modal-con">内容</div>
	<div class="box-hover-modal-m">遮盖层</div>
</div>
```

#### CSS部分
	
	外面的块需要有position属性，内部块使用绝对定位方式，开始隐藏

```css
.box-hover-modal {
	position: relative;
	float: left;
	margin-right: 20px;
	margin-bottom: 20px;
	width: 200px;
	height: 200px;
	background: #aaa;
	overflow: hidden;
}
.box-hover-modal-con {
	width: 100%;
	height: 100%;
}
.box-hover-modal-m {
	display: none;
	position: absolute;
	width: 100%;
	height: 100%;
	top: 0;
	left: 0;
	background: crimson;
}
```

### JAVASCRIPT部分

	使用封装对象方式开发，一个操作对象，一个可选参数

```javascript
//操作对象为.box-hover-modal，可选参数是用来确定modal层的
$(".box-hover-modal").boxhovermodal(".box-hover-modal-m");
```