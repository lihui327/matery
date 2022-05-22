---
title: about
date: 2018-09-30 17:25:30
type: "about"
layout: "about"
---

#### 联系我

邮箱：2322033348@qq.com

#### 个人教育经历

2019~2023	在校大学生

#### 个人目标

> **在学习时能够静下心来学习**
>
> **千锤百炼，终将到达远方。**

#### 名言警句

> **当你刻意地追求时，它就像蝴蝶一样振翅飞远；当你专心致志之时，意外的收获已悄悄来到你的身边。**
>
> **When you pursue something deliberately, it flies**
> **away like a butterfly. When you concentrate, unexpected harvest has quietly come to your**
> **side.**
>
> **只有十分努力，做事才能毫不费力。**
>
> **只有经历了绝望，才能实现真正的超越。**
>
> **再伟大的梦想也抵挡不住最愚蠢的坚持**
>
> **不积跬步，无以至千里；不积小流，无以成江海。**
>
> **谁都不能忘记心中的勇气，更不应该忘记那份勇敢善良的心灵，千锤百炼，你终将成为英雄。**
>
> **三思而后行。**
>
> **能力越大，责任越大。**

#### 楷模

[**C语言中文网站长**](http://c.biancheng.net/view/8092.html). [**菜鸟教程站长**](https://mp.weixin.qq.com/s/sVtChB0SrwmZIwqr5wJARA).

#### 崇拜人物

[**戚继光**](https://baike.baidu.com/item/%E6%88%9A%E7%BB%A7%E5%85%89/22374?fr=aladdin). [**雷欧奥特曼**](https://www.bilibili.com/video/BV1oE411D7GE?share_source=copy_web).

#### 励志视频


<iframe src="//player.bilibili.com/player.html?aid=70236053&bvid=BV1oE411D7GE&cid=121673166&page=1" scrolling="no" border="0" frameborder="no" framespacing="0" allowfullscreen="true" width="600" height="450"> </iframe>

<iframe src="//player.bilibili.com/player.html?aid=58967600&bvid=BV18t411L79T&cid=102790542&page=1" scrolling="no" border="0" frameborder="no" framespacing="0" allowfullscreen="true" width="600" height="450"> </iframe>

#### 个人小工具—密码生成器

<!DOCTYPE html>
<head> 
    <meta http-equiv="Content-Type"content="text/html; charset=UTF-8">
	<!-- <title>lihui327-随机密码生成器</title> -->
</head>
<body>
<table cellspacing=1 cellpadding=1 class="table">
<tr>
	<td class="td_left">选项:</td>
    <td class="td_right"><input id="tools_length"value="8"maxlength="3"style="width:80px;margin-right:2px">位
<input type="checkbox"id="tools_letters_upper"checked="true"style="margin:0 2px 0 30px">
<label for="tools_letters_upper"title="大写字母">A-Z</label>
<input type="checkbox"id="tools_letters_lower"checked="true"style="margin:0 2px 0 30px">
<label for="tools_letters_lower"title="小写字母">a-z</label>
<input type="checkbox"name="tools_numbers"id="tools_numbers"checked="true"style="margin:0 2px 0 30px">
<label for="tools_numbers"title="数字">0-9</label>
<input type="checkbox"id="tools_punctuations"checked="false"style="margin:0 2px 0 30px">
<label for="tools_punctuations"title="符号">符号</label>
   	</td>
</tr>
<tr><td class="td_left">生成结果:</td>
       <td class="td_right"><input style="width:98%;background-color:#f3f3f3"id="tools_result"readonly="true"onfocus="this.select()"></td>
</tr>
<tr><td class="td_left"></td>
       <td class="td_right"><input type="button"id="tools_submit_btn"class="btn"value="生成密码"onclick="password_generator()">
       </td>
</tr>
</table>
<script type="text/javascript">
	function password_generator(){
		var i;
		var j;
		var k;
		var result="";
		var string=new Array();
		string[0]="ABCDEFGHIJKLMNOPQRSTUVWXYZ";
		string[1]="abcdefghijklmnopqrstuvwxyz";
		string[2]="0123456789";
		string[3]="!@#$%^&*()_+~`|}{[]\:;?><,./-=";
		var checkbox_letters_upper=document.getElementById("tools_letters_upper");
		var checkbox_letters_lower=document.getElementById("tools_letters_lower");
		var checkbox_numbers=document.getElementById("tools_numbers");
		var checkbox_punctuations=document.getElementById("tools_punctuations");
		var input_length=document.getElementById("tools_length");
		var input_result=document.getElementById("tools_result");
		var len=parseInt(input_length.value);
		if(len<1){
			len=8;input_length.value="8"
		}
		if(checkbox_letters_upper.checked==false)
		{
			string[0]=""
		}
		if(checkbox_letters_lower.checked==false)
		{
			string[1]=""
		}
		if(checkbox_numbers.checked==false)
		{
			string[2]=""
		}
		if(checkbox_punctuations.checked==false)
		{
			string[3]=""
		}
		if(string.length>0)
		{
			for(i=len;i>0;--i)
			{
				j=Math.floor(Math.random()*4);
				while(string[j]=="")
					j=Math.floor(Math.random()*4);
				k=Math.floor(Math.random()*string[j].length)
				result+=string[j][k];
			}
			input_result.value=result
        }
	}
</script>
</body>
</html>