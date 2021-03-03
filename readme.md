## 记录学习有关 canvas

### day01 绘制图形

```js
// 通过id获取canvas
var canvas = document.getElementById("id");
// 创建画布
var context = canvas.getContext();
// 绘制矩形, x、y 为绘制起点
context.strokeStyle = "#000";
context.strokeRect(x, y, width, height);
// 填充
context.fillStyle = "#000";
context.fillRect(x, y, width, height);

// 开启绘制路径
context.beginPath();
// 路径起点
context.moveTo(x, y);
// 路径结点连线
context.lineTo(x, y);
// 闭环形成
context.closePath();
// 进行绘制
context.stroke();

/**
 *  绘制圆弧
 *  x、y 为圆心坐标
 *  radius为半径
 *  starAngle 为圆弧起点
 *  endAngle 为圆弧终点，
 *  anticlockwise 值为 false 时是顺时针。
 *  正圆为顺时针2 * Math.PI
 */
context.beginPath();
context.arc(x, y, radius, startAngle, endAngle, anticlockwise);
context.fillStyle = "#000";
context.fill();
```
