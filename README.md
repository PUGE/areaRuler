ruler.js
======

### Demo
<a href="Demo page">Demo Page</a>


ruler.js is an HTML5 ruler plugin that provides a set of 'photoshop' like rulers to surround the 'stage' of your authoring tools.
No jquery!
No dependencies!

###Installation
<hr>
<br/>

```terminal
npm install ruler.js --save
```

<br/>
Then
<br/>

```html
<link rel="stylesheet" href="node_modules/ruler.js/dist/ruler.min.css">
<script src="node_modules/ruler.js//dist/ruler.min.js"></script>
```

<br/>

##Getting Started

<hr>
<br/>

```javascript
var myRuler = new ruler({
        container: document.querySelector('#stage'),// 标尺容器
        rulerHeight: 20, // 标尺厚度
        fontFamily: 'arial', // 节点字体
        fontSize: '12px', 
        strokeStyle: 'white',
        lineWidth: 1,
        enableMouseTracking: true,
        enableToolTip: true
    });
```
### Usage 
```javascript
myRuler.api.setPos({x:100, y:100})
/*
改变标尺的坐标点
*/
myRuler.api.scale(1.5);
/*
改变标尺缩放比例
*/
myRuler.api.toggleRulerVisibility(true);
/*
隐藏或者显示标尺
*/
myRuler.api.toggleGuideVisibility(true);
/*
隐藏或者显示标线
*/
myRuler.api.clearGuides(true);
/*
get list of guides to store or copy
*/
myRuler.api.getGuides(); // => [{dimension: number, poxX: number: posY: number}...]
/*
set guides from a pre stored list
*/
myRuler.api.setGuides([{dimension: number, poxX: number: posY: number}...]);
/*
clear all guides
*/
myRuler.api.destory();
/*
remove rulers, guides and references;
*/
```


You can also clear a guide line by double clicking on it or dragging it back to the ruler

### Todo's

Write Tests


License
----

MIT


