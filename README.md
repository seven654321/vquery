#part1:
#
vquery-1.1 兼容性来说还是非常不错，选取速度在ie7下的表现，对于深度为500多的节点，选取速度是jquery(2014-10版本)的2到3倍
vquery-2  不再兼容ie6,7
#
log 表记录了最近一段时间的成长。

focus:
本人目前也只是在学习阶段，欢迎指教，哦，对了，有兴趣的话可以看一下源码，本人目前还没有借鉴jquery的写法，
主要来说是从《javascript设计模式》，《编写可维护的javascript》,《高性能javascipt》中获得的启示


api:
#1
$()
$('div')
$('#div1')
$('.box')
$('div.box1.box2......');
$('.pox1.pox2............')
$('#div1 .pox2.pox3.pox4 .box2.box3.box4');
$('div[name=“jason”]');
#总结支持id,class,tagname,以及多个class,tagname与class复合形式，支持后代选择器
#支持属性选择器
#2
click

#3
hover

#4
animate(json,fn)

For instance:
animate({'width':'500px,'opacity':70,'top':'30px'},function(){alert('ok');})
#注意top,left运动的前提是本身有pos:rea或者pos:abs

#5
show

#6
hide

#7
fadeIn

#8
fadeOut

#9
slideUp

#10
slideDown

#11
css

#12
attr

#13
toggle
For instance:
$('#div1').toggle(fn1,fn2,fn3);
#三个函数会在点击div的时候依次执行

#14
eq()

#15
find()

16
index()

#17
bind()
For instance:
$('#div1').bind('click',fn);

#18
each
#遍历dom节点
For instance:
$('div').each(function(index,value){

   $(this).click(function{
     alert(index);
   });
})

#19
$.each()
#遍历数组
For instance:
$.each(arr1,function(index,value){

   alert(index);
});

#20
onscroll()
For instance:
$('div').onscroll(function(bStop){
   if(bStop)
    {
     console.log('mouse down');
    }
    else
   {
     console.log('mouse up');
    }
},fn2,fn3.....);
#fn2,fn3使用效果跟第一个相同，传入的第一个参数代表鼠标向下滚动

#21
stop()
For instance:
$('#div1').stop();
#可以把正在进行的动作停止



/*
22 到最后的api不支持多个元素的操作，支持单个元素
*/
#22
$('#div1').text();
#23
$('#div1').html();
#24
$('#input1').val();
#25
$('#div1').append();
#26
$('#div1').prepend();
#27
$('#div1').remove();
#28
$('#div1').empty();
#29
$('#div1').width();
#30
$('#div1').height();
#31
$('#div1').innerHeight();
#32
$('#div1').innerWidth;
#33
$('#div1').outerWidth;
#34
$('#div1').outerHeight();
#35
$('#div1').parent();
#36
$('#div1').parents();
#37
$('#div1').parentsUntil('body');
#38
$('#div1').children('ss');
#39
$.ajax('get','2.php','x=123&y=456',function(result)
{
    console.log(result);
});
#40
aboslute
$('div').absolute;
可以更改非绝对定位为绝对定位，满足运动的先期条件，
较少重排
#41
siblings
#42
promise-defer
#43
delegate







