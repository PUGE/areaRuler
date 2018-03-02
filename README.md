areaRuler
======

### Demo
<a href="https://puge.github.io/areaRuler/">示例Demo</a>


为areaRuler指定一个容器，它可以为你创造一个类似于PS的区域标尺！

###安装
<hr>
<br/>

```terminal
npm install arearuler --save
```

<br/>
Then
<br/>

```html
import Ruler from 'ruler.js'
import 'ruler.js/dist/ruler.min.css'
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


