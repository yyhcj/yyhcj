# <center>jquery学习笔记
## 一：简介
jquery是一个JavaScript库，极大简化了js编程
思想是

## 二：使用方法
$(document).ready(function(){
*代码区域*
});

可以简化为
$(function(){
});

$符号是选择的意思  
$("button").click({
})//这样就是选择所有的按钮添加一个点击事件，大括号内写点击事件的函数
$("p").hide();//这样就是选择所有的p元素对其隐藏

完整代码就是这样  
$(function(){
    $("button").click({
        $("p").hide()
    });
});
只用"P"就是选择全部p元素，"#test"就是选择id=test的元素，".test"就是选择class等于test的元素。
![alt text](image.png)

# 三：常用的事件
![alt text](image-1.png)

# 四：各种效果
1. 隐藏展示
   1. 隐藏hide()
   2. 展示show()
   3. 智能替换toggle()
2. 淡入淡出//括号内填速度参数，还可以多填一个执行完后接着执行的函数名
   1. fadeIn()
   2. fadeOut()
   3. fadeToggle()
   4. fadeTo()//用于渐变不同的透明度，两个参数，速度，不透明度（0-1）
3. 滑动//参数和淡入淡出一样
   1. slideDown()
   2. slideUp()
   3. slideToggle()
4. 动画
   1. animate({
   //在里面写要改变的参数，可以是css各个属性
   })
   2. 可以建造一个animate队列，依次执行各个动作
   3. 调整属性值时，属性值要用''包住，实例：
   $("button").click(function(){
  var div=$("div");
  div.animate({height:'300px',opacity:'0.4'},"slow");
  div.animate({width:'300px',opacity:'0.8'},"slow");
  div.animate({height:'100px',opacity:'0.4'},"slow");
  div.animate({width:'100px',opacity:'0.8'},"slow");
});
   4. 停止动画：stop()
   5. 回调函数callback：在动画完成后的行为
   6. 链：可以将多个效果一起执行：$("div").css("color","red").slideDown("fast")
   
   
