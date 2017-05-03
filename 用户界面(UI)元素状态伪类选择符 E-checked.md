﻿# 用户界面(UI)元素状态伪类选择符 E:checked

    <fieldset> <legend> 

---

代码：

    <!DOCTYPE html>
    <html lang="zh-cn">
    <head>
    <meta charset="utf-8" />
    <title></title>
    <style>
    input:checked+span{background:#f00;}
    input:checked+span:after{content:" 我被选中了";}
    </style>
    </head>
    <body>
    <form method="post" action="#">
    <fieldset>
    	<legend>选中下面的项试试</legend>
    	<ul>
    		<li><label><input type="radio" name="colour-group" value="0" /><span>蓝色</span></label></li>
    		<li><label><input type="radio" name="colour-group" value="1" /><span>红色</span></label></li>
    		<li><label><input type="radio" name="colour-group" value="2" /><span>黑色</span></label></li>
    	</ul>
    </fieldset>
    <fieldset>
    	<span>选中下面的项试试</span>
    	<ul>
    		<li><label><input type="checkbox" name="colour-group2" value="0" /><span>蓝色</span></label></li>
    		<li><label><input type="checkbox" name="colour-group2" value="1" /><span>红色</span></label></li>
    		<li><label><input type="checkbox" name="colour-group2" value="2" /><span>黑色</span></label></li>
    	</ul>
    </fieldset>
    </form>
    </body>
    </html>




