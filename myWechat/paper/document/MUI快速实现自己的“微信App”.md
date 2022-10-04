# 2小时使用MUI快速实现自己的“微信App”

# MUI和开发工具介绍

## MUI框架介绍

​	mui是DCLOUD的HTML5混合移动应用前端框架，mui技术是最接近原生App体验的前端框架。使用mui框架可以快速搭建手机移动原生界面应用开发，配合着Hbuilder开发工具可以达到更加快速的开发模式。

MUI特点：

1. 极小

   100k的js文件，60k的css文件。原生编写，不依赖任何三方框架

2. 极强

   xcode和Android studio里所有原生控件都具备。(http://dev.dcloud.net.cn/mui/)

3. 高性能

   精练的代码、适时的5+原生动画调用，达到原生应用的体验

4. 多端发布

   编写一套代码，iOS、Android、浏览器、微信App、百度直达号、流应用全覆盖

官网地址：http://www.dcloud.io/mui.html

![](img/1.png)

## HBuilder开发工具介绍

下载：http://www.dcloud.io/

![](img/2.png)

HBuilder是DCloud（数字天堂）推出的一款支持HTML5的Web开发IDE。HBuilder的编写用到了Java、C、Web和Ruby。HBuilder本身主体是由Java编写。它基于Eclipse，所以顺其自然地兼容了Eclipse的插件。数字天堂公司是HTML5联盟成员，在前端方面非常具有权威的。

开发工具特点：

- 编码比其他工具快5倍够不够？对极客而言，追求快，没有止境！
- 代码输入法：按下数字快速选择候选项
- 可编程代码块：一个代码块，少敲50个按键
- 内置emmet：tab一下生成一串代码
- 无死角提示：除了语法，还能提示ID、Class、图片、链接、字体…
- 跳转助手、选择助手，不用鼠标，手不离键盘
- 多种语言支持：php、jsp、ruby、python、nodejs等web语言，less、coffee等编译型语言均支持
- 边改边看：一边写代码，一边看效果
- 强悍的转到定义和一键搜索
- 这里还有最全的语法库、最全的语法浏览器兼容库

# MUI开发体验

## 体验效果

![](img/3.png)

## 实现步骤

1. 创建项目

   ![](img/4.png)

2. 创建项目的资源结构和首页代码

   ![](img/5.png)

3. 在首页index.html中完成页面工具栏，操作如下

   ![](img/6.png)

4. 完成如下代码

   ```html
   <!DOCTYPE html>
   <html>
   <head>
       <meta charset="utf-8">
       <meta name="viewport" content="width=device-width,initial-scale=1,minimum-scale=1,maximum-scale=1,user-scalable=no" />
       <title></title>
       <script src="js/mui.min.js"></script>
       <link href="css/mui.min.css" rel="stylesheet"/>
       <script type="text/javascript" charset="utf-8">
         	mui.init();
       </script>
   </head>
   <body>
   	<!--顶部标题工具栏-->
   	<header class="mui-bar mui-bar-nav">
   	    <a class="mui-action-back mui-icon mui-icon-left-nav mui-pull-left"></a>
   	    <h1 class="mui-title">微信</h1>
   	</header>
   	<!--中间好友列表-->
   	<ul class="mui-table-view">
   	    <li class="mui-table-view-cell mui-media">
   	        <a href="javascript:;">
   	            <img class="mui-media-object mui-pull-left" src="img/1.jpg">
   	            <div class="mui-media-body">
   	                幸福
   	                <p class="mui-ellipsis">能和心爱的人一起睡觉，是件幸福的事情；可是，打呼噜怎么办？</p>
   	            </div>
   	        </a>
   	    </li>
   	    <li class="mui-table-view-cell mui-media">
   	        <a href="javascript:;">
   	            <img class="mui-media-object mui-pull-left" src="img/2.jpg">
   	            <div class="mui-media-body">
   	                木屋
   	                <p class="mui-ellipsis">想要这样一间小木屋，夏天挫冰吃瓜，冬天围炉取暖.</p>
   	            </div>
   	        </a>
   	    </li>
   	    <li class="mui-table-view-cell mui-media">
   	        <a href="javascript:;">
   	            <img class="mui-media-object mui-pull-left" src="img/3.jpg">
   	            <div class="mui-media-body">
   	               清晰
   	                <p class="mui-ellipsis">烤炉模式的城，到黄昏，如同打翻的调色盘一般.</p>
   	            </div>
   	        </a>
   	    </li>
   	    <li class="mui-table-view-cell mui-media">
   	        <a href="javascript:;">
   	            <img class="mui-media-object mui-pull-left" src="img/4.jpg">
   	            <div class="mui-media-body">
   	                脱俗
   	                <p class="mui-ellipsis">烤炉模式的城，到黄昏，如同打翻的调色盘一般.</p>
   	            </div>
   	        </a>
   	    </li>
   	    <li class="mui-table-view-cell mui-media">
   	        <a href="javascript:;">
   	            <img class="mui-media-object mui-pull-left" src="img/5.jpg">
   	            <div class="mui-media-body">
   	                甘露
   	                <p class="mui-ellipsis">烤炉模式的城，到黄昏，如同打翻的调色盘一般.</p>
   	            </div>
   	        </a>
   	    </li>
   	</ul>
   	<!--底部导航栏-->
   	<nav class="mui-bar mui-bar-tab">
   	    <a class="mui-tab-item mui-active">
   	        <span class="mui-icon mui-icon-home"></span>
   	        <span class="mui-tab-label">首页</span>
   	    </a>
   	    <a class="mui-tab-item">
   	        <span class="mui-icon mui-icon-phone"></span>
   	        <span class="mui-tab-label">电话</span>
   	    </a>
   	    <a class="mui-tab-item">
   	        <span class="mui-icon mui-icon-email"></span>
   	        <span class="mui-tab-label">邮件</span>
   	    </a>
   	    <a class="mui-tab-item">
   	        <span class="mui-icon mui-icon-gear"></span>
   	        <span class="mui-tab-label">设置</span>
   	    </a>
   	</nav>
   </body>
   </html>
   ```

演示

| 快速输入命令 | 说明                               |
| ------ | -------------------------------- |
| mh     | 快速生成标题栏                          |
| ml     | 快速图文列表                           |
| mt     | 底部工具类导航列表                        |
| mb     | 页面主体，设置手机主要区域内容展现优化，将图文列表放到页面主体内 |

# 微信好友列表页面优化

## 顶部标题栏优化

效果

![](img/7.png)

创建样式表

![](img/10.png)

index.html页面引入样式文件代码

```html
<link rel="stylesheet" type="text/css" href="css/main.css"/>
```

## 底部Tab导航图标优化

效果

![](img/12.png)

访问http://dev.dcloud.net.cn/mui/ui/#icon，mui内置的图标，如下图

![](img/11.png)

代码如下：

```html
<!--底部导航栏-->
	<nav class="mui-bar mui-bar-tab">
	    <a class="mui-tab-item mui-active">
	        <span class="mui-icon mui-icon-chatbubble"></span>
	        <span class="mui-tab-label">微信</span>
	    </a>
	    <a class="mui-tab-item">
	        <span class="mui-icon mui-icon-contact"></span>
	        <span class="mui-tab-label">通信录</span>
	    </a>
	    <a class="mui-tab-item">
	        <span class="mui-icon mui-icon-navigate"></span>
	        <span class="mui-tab-label">发现</span>
	    </a>
	    <a class="mui-tab-item">
	        <span class="mui-icon mui-icon-person"></span>
	        <span class="mui-tab-label">我</span>
	    </a>
	</nav>
```

# 创建子页面实	现导航切换页面 

## 实现效果

![](img/19.png)

## 创建子页面

页面结构，创建子页面sub1.html,sub2.html,sub3.html,sub4.html

![](img/15.png)

sub1.html(微信好友子页面)

```html
<!doctype html>
<html>

	<head>
		<meta charset="UTF-8">
		<title></title>
		<meta name="viewport" content="width=device-width,initial-scale=1,minimum-scale=1,maximum-scale=1,user-scalable=no" />
		<link href="css/mui.min.css" rel="stylesheet" />
	</head>

	<body>
		<script src="js/mui.min.js"></script>
		<script type="text/javascript">
			mui.init()
		</script>
		<!--中间好友列表-->
	<div class="mui-content">
	    <ul class="mui-table-view">
	    <li class="mui-table-view-cell mui-media">
	        <a href="javascript:;">
	            <img class="mui-media-object mui-pull-left" src="img/1.jpg">
	            <div class="mui-media-body">
	                幸福
	                <p class="mui-ellipsis">能和心爱的人一起睡觉，是件幸福的事情；可是，打呼噜怎么办？</p>
	            </div>
	        </a>
	    </li>
	    <li class="mui-table-view-cell mui-media">
	        <a href="javascript:;">
	            <img class="mui-media-object mui-pull-left" src="img/2.jpg">
	            <div class="mui-media-body">
	                木屋
	                <p class="mui-ellipsis">想要这样一间小木屋，夏天挫冰吃瓜，冬天围炉取暖.</p>
	            </div>
	        </a>
	    </li>
	    <li class="mui-table-view-cell mui-media">
	        <a href="javascript:;">
	            <img class="mui-media-object mui-pull-left" src="img/3.jpg">
	            <div class="mui-media-body">
	               清晰
	                <p class="mui-ellipsis">烤炉模式的城，到黄昏，如同打翻的调色盘一般.</p>
	            </div>
	        </a>
	    </li>
	    <li class="mui-table-view-cell mui-media">
	        <a href="javascript:;">
	            <img class="mui-media-object mui-pull-left" src="img/4.jpg">
	            <div class="mui-media-body">
	                脱俗
	                <p class="mui-ellipsis">烤炉模式的城，到黄昏，如同打翻的调色盘一般.</p>
	            </div>
	        </a>
	    </li>
	    <li class="mui-table-view-cell mui-media">
	        <a href="javascript:;">
	            <img class="mui-media-object mui-pull-left" src="img/5.jpg">
	            <div class="mui-media-body">
	         及时雨
	                <p class="mui-ellipsis">烤炉模式的城，到黄昏，如同打翻的调色盘一般.</p>
	            </div>
	        </a>
	    </li>
	</ul>
	</div>
	</body>

</html>
```

sub2.html（通信录子页面）

```html
<!doctype html>
<html>

	<head>
		<meta charset="UTF-8">
		<title></title>
		<meta name="viewport" content="width=device-width,initial-scale=1,minimum-scale=1,maximum-scale=1,user-scalable=no" />
		<link href="css/mui.min.css" rel="stylesheet" />
	</head>

	<body>
		<script src="js/mui.min.js"></script>
		<script type="text/javascript">
			mui.init()
		</script>
	<div class="mui-content">
	   通信录
	</div>
	</body>

</html>
```

sub3.html（发现子页面）

```html
<!doctype html>
<html>

	<head>
		<meta charset="UTF-8">
		<title></title>
		<meta name="viewport" content="width=device-width,initial-scale=1,minimum-scale=1,maximum-scale=1,user-scalable=no" />
		<link href="css/mui.min.css" rel="stylesheet" />
	</head>

	<body>
		<script src="js/mui.min.js"></script>
		<script type="text/javascript">
			mui.init()
		</script>
	<div class="mui-content">
	   发现
	</div>
	</body>

</html>
```

sub4.html（我，个人中心子页面）

```html
<!doctype html>
<html>

	<head>
		<meta charset="UTF-8">
		<title></title>
		<meta name="viewport" content="width=device-width,initial-scale=1,minimum-scale=1,maximum-scale=1,user-scalable=no" />
		<link href="css/mui.min.css" rel="stylesheet" />
	</head>

	<body>
		<script src="js/mui.min.js"></script>
		<script type="text/javascript">
			mui.init()
		</script>
	<div class="mui-content">
	   我
	</div>
	</body>

</html>
```

## 手机导航栏目切换子页面原理

手机显示web网页是通过webView手机原生界面实现的。

WebView手机原生界面

​	WebView是手机展现web页面的控件。手机显示一个web网页，需要根据网页创建WebView,手机就可以显示webView里面的web页面了。

![](img/28.png)

## 使用WebView创建子页面



```html
<!DOCTYPE html>
<html>
<head>
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width,initial-scale=1,minimum-scale=1,maximum-scale=1,user-scalable=no" />
    <title></title>
    <script src="js/mui.min.js"></script>
    <link href="css/mui.min.css" rel="stylesheet"/>
    <link rel="stylesheet" type="text/css" href="css/main.css"/>
    <script type="text/javascript" charset="utf-8">
      	mui.init();
    </script>
    <script type="text/javascript">
    	//定义子页面url数组
    	var subPages = ["sub1.html","sub2.html","sub3.html","sub4.html"];
    	//设置每个页面通用样式
    	var subPageStyle = {
    		top:"44px",
    		bottom:"50px"
    	};
    	//mui加载完毕后的回调函数，在函数里面加载所有子页面
    	mui.plusReady(function(){
    		//获得手机显示页面的webView硬件对象（
    		var curWebView = plus.webview.currentWebview();
    		//遍历子页面url数组
    		for(var i=0;i<subPages.length;i++){
    			//创建子页面的webView对象,语法：plus.webview.create(url,id,style)
    			//参数1：url,指定具体页面地址
    			//参数2：id,页面的位置标识符
    			//参数3：style,当前页面要应用的样式
    			var subPageWebView = plus.webview.create(subPages[i],subPages[i],subPageStyle);
    			//设置子页面的webView页面对象默认隐藏（所有子页面默认隐藏）
    			subPageWebView.hide();
    			//将子页面装载到webView中
    			curWebView.append(subPageWebView);
    		}
    		//默认显示第一个子页面
    		plus.webview.show(subPages[0]);
    	});
    	
    </script>
</head>
<body>
	<!--顶部标题工具栏-->
	<header class="mui-bar mui-bar-nav">
	    <a class="mui-action-back mui-icon mui-icon-left-nav mui-pull-left"></a>
	    <h1 class="mui-title">微信</h1>
	</header>
	
	
	<!--底部导航栏-->
	<nav class="mui-bar mui-bar-tab">
	    <a class="mui-tab-item mui-active">
	        <span class="mui-icon mui-icon-chatbubble"></span>
	        <span class="mui-tab-label">微信</span>
	    </a>
	    <a class="mui-tab-item">
	        <span class="mui-icon mui-icon-contact"></span>
	        <span class="mui-tab-label">通信录</span>
	    </a>
	    <a class="mui-tab-item">
	        <span class="mui-icon mui-icon-navigate"></span>
	        <span class="mui-tab-label">发现</span>
	    </a>
	    <a class="mui-tab-item">
	        <span class="mui-icon mui-icon-person"></span>
	        <span class="mui-tab-label">我</span>
	    </a>
	</nav>
</body>
</html>
```

## 安装夜神模拟器

模拟器：模拟一台真实手机系统运行。

1. 根据提供资料“nox_setup_v6.0.6.1_full.exe”软件，全部下一步进行默认安装

2. 启动夜神模拟器

   ![](img/18.png)

## 配置hbuilder连接夜神模拟器

```
由于HBuilder的自动扫描机制无法直接连上夜神模拟器，需要通过cmd命令窗口手动处理，才能将两者建立连接。

首先，启动HBuilder和夜神模拟器 
然后，打开cmd命令提示符 
cd进入夜神模拟器安装bin目录 （D:\Nox\bin，我本机）
执行以下命令 
nox_adb connect 127.0.0.1:62001 
nox_adb devices
```

![](img/13.png)

```
然后cd进入HBuilder的adbs目录 （D:\HBuilder\tools\adbs，我本机）
执行以下命令 
adb connect 127.0.0.1:62001 
adb devices
```

![](img/14.png)

真机运行步骤：

点击如图真机运行

![](img/17.png)

模拟器运行效果：

![](img/16.png)

## 底部导航进行子页面切换

4.6.1 实现分析

手机app里面的点击不同的导航切换子页面，与pc端不同，pc端是通过a标签连接打开，但是手机app打开子页面需要控制webView页面的显示，什么时候控制webView显示呢？在导航栏点击的时候，但是注意手机硬件原生不没有鼠标点击onclick事件，而是通过人轻击导航栏，这个行为就是手机里面的tap轻击事件。所以得出给底部导航不同栏目注册tap轻击事件，在事件内控制webView显示对应子页面。

4.6.2 实现步骤

1. 给每个导航栏目标签a增加属性href=“子页面地址”，后面用于获取使用

   ```html
   <!--底部导航栏-->
   	<nav class="mui-bar mui-bar-tab">
   	    <a class="mui-tab-item mui-active" href="sub1.html">
   	        <span class="mui-icon mui-icon-chatbubble"></span>
   	        <span class="mui-tab-label">微信</span>
   	    </a>
   	    <a class="mui-tab-item" href="sub2.html">
   	        <span class="mui-icon mui-icon-contact"></span>
   	        <span class="mui-tab-label">通信录</span>
   	    </a>
   	    <a class="mui-tab-item" href="sub3.html">
   	        <span class="mui-icon mui-icon-navigate"></span>
   	        <span class="mui-tab-label">发现</span>
   	    </a>
   	    <a class="mui-tab-item" href="sub4.html">
   	        <span class="mui-icon mui-icon-person"></span>
   	        <span class="mui-tab-label">我</span>
   	    </a>
   	</nav>
   ```

2. 在mui加载事件里面，给每个导航a标签注册tap轻击事件

   ```javascript
   //给每个导航a注册手机移动轻击事件
   mui(".mui-bar-tab").on("tap","a",function(){
   	...
   });
   ```

3. 事件里面获取事件源属性href的值，就是要打开页面的地址，控制硬件显示这个地址的webView页面

   ```javascript
   //给每个导航a注册手机移动轻击事件
   mui(".mui-bar-tab").on("tap","a",function(){
       //获取每个a标签的href属性值，子页面地址
       var url = this.getAttribute("href");
       //设置对应子页面webView显示
       plus.webview.show(url);
   });
   ```

   ​

4.6.3 完整代码

```
<!DOCTYPE html>
<html>
<head>
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width,initial-scale=1,minimum-scale=1,maximum-scale=1,user-scalable=no" />
    <title></title>
    <script src="js/mui.min.js"></script>
    <link href="css/mui.min.css" rel="stylesheet"/>
    <link rel="stylesheet" type="text/css" href="css/main.css"/>
    <script type="text/javascript" charset="utf-8">
      	mui.init();
    </script>
    <script type="text/javascript">
    	//定义子页面url数组
    	var subPages = ["sub1.html","sub2.html","sub3.html","sub4.html"];
    	//设置每个页面通用样式
    	var subPageStyle = {
    		top:"44px",
    		bottom:"50px"
    	};
    	//mui加载完毕后的回调函数，在函数里面加载所有子页面
    	mui.plusReady(function(){
    		//获得手机显示页面的webView硬件对象（
    		var curWebView = plus.webview.currentWebview();
    		//遍历子页面url数组
    		for(var i=0;i<subPages.length;i++){
    			//创建子页面的webView对象,语法：plus.webview.create(url,id,style)
    			//参数1：url,指定具体页面地址
    			//参数2：id,页面的位置标识符
    			//参数3：style,当前页面要应用的样式
    			var subPageWebView = plus.webview.create(subPages[i],subPages[i],subPageStyle);
    			//设置子页面的webView页面对象默认隐藏（所有子页面默认隐藏）
    			subPageWebView.hide();
    			//将子页面装载到webView中
    			curWebView.append(subPageWebView);
    		}
    		//默认显示第一个子页面
    		plus.webview.show(subPages[0]);
    		
    		//给每个导航a注册手机移动轻击事件
	    	mui(".mui-bar-tab").on("tap","a",function(){
	    		//获取每个a标签的href属性值，子页面地址
	    		var url = this.getAttribute("href");
	    		//设置对应子页面webView显示
	    		plus.webview.show(url);
	    	});
    	});
    	
    	
    </script>
</head>
<body>
	<!--顶部标题工具栏-->
	<header class="mui-bar mui-bar-nav">
	    <a class="mui-action-back mui-icon mui-icon-left-nav mui-pull-left"></a>
	    <h1 class="mui-title">微信</h1>
	</header>
	
	
	<!--底部导航栏-->
	<nav class="mui-bar mui-bar-tab">
	    <a class="mui-tab-item mui-active" href="sub1.html">
	        <span class="mui-icon mui-icon-chatbubble"></span>
	        <span class="mui-tab-label">微信</span>
	    </a>
	    <a class="mui-tab-item" href="sub2.html">
	        <span class="mui-icon mui-icon-contact"></span>
	        <span class="mui-tab-label">通信录</span>
	    </a>
	    <a class="mui-tab-item" href="sub3.html">
	        <span class="mui-icon mui-icon-navigate"></span>
	        <span class="mui-tab-label">发现</span>
	    </a>
	    <a class="mui-tab-item" href="sub4.html">
	        <span class="mui-icon mui-icon-person"></span>
	        <span class="mui-tab-label">我</span>
	    </a>
	</nav>
</body>
</html>
```



# 聊天页面开发

## 效果

打开页面并传递数据

![](img/20.png)

发送文本数据效果

![](img/22.png)

发送图片数据效果

![](img/23.png)

## 打开聊天页面并传递数据

### 实现步骤

1. chat.html页面，新建一个child目录，根据提供的素材页面chat.html导入到child目录

   ![](img/21.png)

2. sub1.html页面代码，给每个好友标签a注册轻击事件，使用openwindow方法打开新页面，并传递好友名称

3. chat.html页面代码，mui页面加载完成事件里面获得传递过来的好友名称，并设置到当前页面顶部标题位置

### 实现代码

sub1.html页面代码

```html
<!doctype html>
<html>

	<head>
		<meta charset="UTF-8">
		<title></title>
		<meta name="viewport" content="width=device-width,initial-scale=1,minimum-scale=1,maximum-scale=1,user-scalable=no" />
		<link href="css/mui.min.css" rel="stylesheet" />
	</head>

	<body>
		<script src="js/mui.min.js"></script>
		<script type="text/javascript">
			mui.init();
			
			//加载事件
			mui.ready(function(){
				
				//注册轻击事件
				mui(".mui-table-view-cell").on("tap","a",function(){
					//获得好友名称进行传递
					var title = this.getAttribute("title");
					mui.openWindow({
						url:"child/chat.html",
						id:"child/chat.html",
						show:{
							autoShow:true,
							aniShow:"slide-in-right",
							duration:100
						},
						waiting:{
							auto:true,
							title:"正在加载.."
						},
						extras:{
							title:title
						}
						
					})
				});
				
			});
		</script>
		<!--中间好友列表-->
	<div class="mui-content">
	    <ul class="mui-table-view">
	    <li class="mui-table-view-cell mui-media" title="幸福">
	        <a href="javascript:;">
	            <img class="mui-media-object mui-pull-left" src="img/1.jpg">
	            <div class="mui-media-body">
	                幸福
	                <p class="mui-ellipsis">能和心爱的人一起睡觉，是件幸福的事情；可是，打呼噜怎么办？</p>
	            </div>
	        </a>
	    </li>
	    <li class="mui-table-view-cell mui-media" >
	        <a href="javascript:;" title="木屋">
	            <img class="mui-media-object mui-pull-left" src="img/2.jpg">
	            <div class="mui-media-body">
	                木屋
	                <p class="mui-ellipsis">想要这样一间小木屋，夏天挫冰吃瓜，冬天围炉取暖.</p>
	            </div>
	        </a>
	    </li>
	    <li class="mui-table-view-cell mui-media">
	        <a href="javascript:;" title="清晰">
	            <img class="mui-media-object mui-pull-left" src="img/3.jpg">
	            <div class="mui-media-body">
	               清晰
	                <p class="mui-ellipsis">烤炉模式的城，到黄昏，如同打翻的调色盘一般.</p>
	            </div>
	        </a>
	    </li>
	    <li class="mui-table-view-cell mui-media" >
	        <a href="javascript:;" title="脱俗">
	            <img class="mui-media-object mui-pull-left" src="img/4.jpg">
	            <div class="mui-media-body">
	                脱俗
	                <p class="mui-ellipsis">烤炉模式的城，到黄昏，如同打翻的调色盘一般.</p>
	            </div>
	        </a>
	    </li>
	    <li class="mui-table-view-cell mui-media">
	        <a href="javascript:;" title="及时雨">
	            <img class="mui-media-object mui-pull-left" src="img/5.jpg">
	            <div class="mui-media-body">
	         及时雨
	                <p class="mui-ellipsis">烤炉模式的城，到黄昏，如同打翻的调色盘一般.</p>
	            </div>
	        </a>
	    </li>
	</ul>
	</div>
	</body>

</html>
```

chat.html页面代码

```html
<!DOCTYPE html>
<html>

	<head>
		<meta charset="utf-8">
		<meta name="viewport" content="width=device-width,initial-scale=1,minimum-scale=1,maximum-scale=1,user-scalable=no" />
		<title></title>
		<link href="../css/mui.min.css" rel="stylesheet" />
		<style>
			/*
 *这是单独为hello mui准备的个性化css，可以覆盖标准mui的css定义；
 * 在实际项目开发时，建议为App单独写一个css文件，从而实现项目的自定义皮肤功能；
 * 
 * */
			
			.mui-plus.mui-android header.mui-bar {
				float: left;
			}
			
			.mui-plus.mui-android .mui-bar-nav~.mui-content {
				padding-top: 41px;
			}
			
			.mui-active .mui-icon,
			.mui-tab-label {
				color: #45C018;
			}
			/*hm开头的表示仅为 Hello MUI示例定义*/
			
			.hm-description {
				margin: .5em 0;
			}
			
			.hm-description>li {
				font-size: 14px;
				color: #8f8f94;
			}
			
			.mui-bar-nav {
				background: #393a3e;
			}
			
			.mui-icon-arrowthinleft,
			.mui-pull-left,
			.mui-pull-right {
				color: white;
			}
			
			.mui-icon-mic {
				padding-left: 5px;
				float: left;
			}
			
			html,
			body {
				height: 100%;
				overflow: hidden;
			}
			
			.mui-bar {
				-webkit-box-shadow: none;
				box-shadow: none;
			}
			
			.faxianListMedia {
				height: 30px;
				line-height: 30px;
				overflow: hidden;
				float: left;
				padding-left: 15px;
			}
			
			.faxianImage {
				width: 30px;
				height: 30px;
				float: left;
			}
			
			html,
			body {
				height: 100%;
				margin: 0px;
				padding: 0px;
				overflow: hidden;
				-webkit-touch-callout: none;
				-webkit-user-select: none;
			}
			
			footer {
				position: fixed;
				width: 100%;
				height: 50px;
				min-height: 50px;
				border-top: solid 1px #bbb;
				left: 0px;
				bottom: 0px;
				overflow: hidden;
				padding: 0px 50px;
				background-color: #fafafa;
			}
			
			.footer-left {
				position: absolute;
				width: 50px;
				height: 50px;
				left: 0px;
				/*bottom: 0px;*/
				text-align: center;
				vertical-align: middle;
				line-height: 100%;
				padding: 12px 4px;
			}
			
			.footer-right {
				position: absolute;
				width: 50px;
				height: 50px;
				right: 0px;
				bottom: 0px;
				text-align: center;
				vertical-align: middle;
				line-height: 100%;
				padding: 12px 5px;
				display: inline-block;
			}
			
			.footer-center {
				height: 100%;
				padding: 5px 0px;
			}
			
			.footer-center [class*=input] {
				width: 100%;
				height: 100%;
				border-radius: 5px;
			}
			
			.footer-center .input-text {
				background: #fff;
				border: solid 1px #ddd;
				padding: 10px !important;
				font-size: 16px !important;
				line-height: 18px !important;
				font-family: verdana !important;
				overflow: hidden;
			}
			
			.footer-center .input-sound {
				background-color: #eee;
			}
			
			.mui-content {
				height: 100%;
				padding: 44px 0px 50px 0px;
				overflow: auto;
				background-color: #eaeaea;
			}
			
			#msg-list {
				height: 100%;
				overflow: auto;
				-webkit-overflow-scrolling: touch;
			}
			
			.msg-item {
				padding: 8px;
				clear: both;
			}
			
			.msg-item .mui-item-clear {
				clear: both;
			}
			
			.msg-item .msg-user {
				width: 38px;
				height: 38px;
				border: solid 1px #d3d3d3;
				display: inline-block;
				background: #fff;
				border-radius: 3px;
				vertical-align: top;
				text-align: center;
				float: left;
				padding: 3px;
				color: #ddd;
			}
			
			.msg-item .msg-user-img {
				width: 38px;
				height: 38px;
				display: inline-block;
				border-radius: 3px;
				vertical-align: top;
				text-align: center;
				float: left;
				color: #ddd;
			}
			
			.msg-item .msg-content {
				display: inline-block;
				border-radius: 5px;
				border: solid 1px #d3d3d3;
				background-color: #FFFFFF;
				color: #333;
				padding: 8px;
				vertical-align: top;
				font-size: 15px;
				position: relative;
				margin: 0px 8px;
				max-width: 75%;
				min-width: 35px;
				float: left;
			}
			
			.msg-item .msg-content .msg-content-inner {
				overflow-x: hidden;
			}
			
			.msg-item .msg-content .msg-content-arrow {
				position: absolute;
				border: solid 1px #d3d3d3;
				border-right: none;
				border-top: none;
				background-color: #FFFFFF;
				width: 10px;
				height: 10px;
				left: -5px;
				top: 12px;
				-webkit-transform: rotateZ(45deg);
				transform: rotateZ(45deg);
			}
			
			.msg-item-self .msg-user,
			.msg-item-self .msg-content {
				float: right;
			}
			
			.msg-item-self .msg-content .msg-content-arrow {
				left: auto;
				right: -5px;
				-webkit-transform: rotateZ(225deg);
				transform: rotateZ(225deg);
			}
			
			.msg-item-self .msg-content,
			.msg-item-self .msg-content .msg-content-arrow {
				background-color: #4CD964;
				color: #fff;
				border-color: #2AC845;
			}
			
			footer .mui-icon {
				color: #000;
			}
			
			footer .mui-icon:active {
				color: #007AFF !important;
			}
			
			footer .mui-icon-paperplane:before {
				content: "发送";
			}
			
			footer .mui-icon-paperplane {
				/*-webkit-transform: rotateZ(45deg);
				transform: rotateZ(45deg);*/
				font-size: 16px;
				word-break: keep-all;
				line-height: 100%;
				padding-top: 6px;
				color: rgba(0, 135, 250, 1);
			}
			
			#msg-sound {
				-webkit-user-select: none !important;
				user-select: none !important;
			}
			
			.rprogress {
				position: absolute;
				left: 50%;
				top: 50%;
				width: 140px;
				height: 140px;
				margin-left: -70px;
				margin-top: -70px;
				background-image: url(../images/arecord.png);
				background-repeat: no-repeat;
				background-position: center center;
				background-size: 30px 30px;
				background-color: rgba(0, 0, 0, 0.7);
				border-radius: 5px;
				display: none;
				-webkit-transition: .15s;
			}
			
			.rschedule {
				background-color: rgba(0, 0, 0, 0);
				border: 5px solid rgba(0, 183, 229, 0.9);
				opacity: .9;
				border-left: 5px solid rgba(0, 0, 0, 0);
				border-right: 5px solid rgba(0, 0, 0, 0);
				border-radius: 50px;
				box-shadow: 0 0 15px #2187e7;
				width: 46px;
				height: 46px;
				position: absolute;
				left: 50%;
				top: 50%;
				margin-left: -23px;
				margin-top: -23px;
				-webkit-animation: spin 1s infinite linear;
				animation: spin 1s infinite linear;
			}
			
			.r-sigh {
				display: none;
				border-radius: 50px;
				box-shadow: 0 0 15px #2187e7;
				width: 46px;
				height: 46px;
				position: absolute;
				left: 50%;
				top: 50%;
				margin-left: -23px;
				margin-top: -23px;
				text-align: center;
				line-height: 46px;
				font-size: 40px;
				font-weight: bold;
				color: #2187e7;
			}
			
			.rprogress-sigh {
				background-image: none !important;
			}
			
			.rprogress-sigh .rschedule {
				display: none !important;
			}
			
			.rprogress-sigh .r-sigh {
				display: block !important;
			}
			
			.rsalert {
				font-size: 12px;
				color: #bbb;
				text-align: center;
				position: absolute;
				border-radius: 5px;
				width: 130px;
				margin: 5px 5px;
				padding: 5px;
				left: 0px;
				bottom: 0px;
			}
			
			@-webkit-keyframes spin {
				0% {
					-webkit-transform: rotate(0deg);
				}
				100% {
					-webkit-transform: rotate(360deg);
				}
			}
			
			@keyframes spin {
				0% {
					transform: rotate(0deg);
				}
				100% {
					transform: rotate(360deg);
				}
			}
			
			#h {
				background: #fff;
				border: solid 1px #ddd;
				padding: 10px !important;
				font-size: 16px !important;
				font-family: verdana !important;
				line-height: 18px !important;
				overflow: visible;
				position: absolute;
				left: -1000px;
				right: 0px;
				word-break: break-all;
				word-wrap: break-word;
			}
			
			.cancel {
				background-color: darkred;
			}
			.mui-bar-tab{display:inline;height:auto;}
		</style>
		<link rel="stylesheet" type="text/css" href="css/main.css" />
	</head>

    <body contextmenu="return false;">
        <header class="mui-bar mui-bar-nav">
            <a class="mui-action-back mui-icon mui-icon-left-nav mui-pull-left" id="title"></a>
        </header>
        <pre id='h'></pre>

        <div class="mui-content">
            <div id='msg-list'>
                <!--好友发送图片格式-->
                <div class="msg-item 1msg-item-self1 msg-type msg-content">

                    <img class="msg-user-img" src="../img/1.jpg" alt="" />

                    <div class="msg-content">
                        <div class="msg-content-inner">

                            <img class="msg-content-image" src="../img/4.jpg" style="max-width: 100px;" />

                        </div>
                        <div class="msg-content-arrow"></div>
                    </div>
                    <div class="mui-item-clear"></div>
                </div>
                <!--好友的文本格式-->
                <div class="msg-item msg-item-self1 msg-type msg-content">
                    <img class="msg-user-img" src="../img/1.jpg" alt="" />
                    <div class="msg-content">
                        <div class="msg-content-inner">
                            你好
                        </div>
                        <div class="msg-content-arrow"></div>
                    </div>
                    <div class="mui-item-clear"></div>
                </div>
                <!--自己的文本格式
<div class="msg-item msg-item-self msg-content">
<img class="msg-user-img" src="../img/2.jpg" style="float:right" />
<div class="msg-content">
<div class="msg-content-inner">
你好
</div>
<div class="msg-content-arrow"></div>
</div>
<div class="mui-item-clear"></div>
</div>
-->

                <!--自己发送图片格式
<div class="msg-item msg-item-self msg-type msg-content">

<img class="msg-user-img" src="../img/2.jpg" alt="" style="float: right;" />

<div class="msg-content">
<div class="msg-content-inner">

<img class="msg-content-image" src="../img/4.jpg" style="max-width: 100px;" />

</div>
<div class="msg-content-arrow"></div>
</div>
<div class="mui-item-clear"></div>
</div>
-->
            </div>





        </div>

        <!--底部发送消息内容-->
        <nav class="mui-bar mui-bar-tab" style="padding-top: 15px;">
            <i id='msg-image' class="mui-icon mui-icon-plus" style="font-size: 28px;float:left;width:15%;padding-left:10px;"></i>
            <textarea id='msg-text' type="text" class='input-text' style="float:left;width:70%;height:50px;border-radius:10px;"></textarea>
            <i id='msg-type' class="mui-icon mui-icon-paperplane" style="float:left;width:15%;padding-left:10px;"></i>

            <!--九宫格内容-->
            <div id="Gallery" class="mui-slider" style="margin-top:15px;display: none;">
                <div class="mui-slider-group">
                    <div class="mui-slider-item">
                        <ul class="mui-table-view mui-grid-view mui-grid-9">
                            <li class="mui-table-view-cell mui-media mui-col-xs-4 mui-col-sm-4">
                                <a href="#">
                                    <span class="mui-icon mui-icon-image"></span>
                                    <div class="mui-media-body">相册</div>
                                </a>
                            </li>
                            <li class="mui-table-view-cell mui-media mui-col-xs-4 mui-col-sm-4">
                                <a href="#">
                                    <span class="mui-icon mui-icon-email"><span class="mui-badge">5</span></span>
                                    <div class="mui-media-body">Email</div>
                                </a>
                            </li>
                            <li class="mui-table-view-cell mui-media mui-col-xs-4 mui-col-sm-4">
                                <a href="#">
                                    <span class="mui-icon mui-icon-chatbubble"></span>
                                    <div class="mui-media-body">Chat</div>
                                </a>
                            </li>
                            <li class="mui-table-view-cell mui-media mui-col-xs-4 mui-col-sm-4">
                                <a href="#">
                                    <span class="mui-icon mui-icon-location"></span>
                                    <div class="mui-media-body">location</div>
                                </a>
                            </li>
                            <li class="mui-table-view-cell mui-media mui-col-xs-4 mui-col-sm-4">
                                <a href="#">
                                    <span class="mui-icon mui-icon-search"></span>
                                    <div class="mui-media-body">Search</div>
                                </a>
                            </li>
                            <li class="mui-table-view-cell mui-media mui-col-xs-4 mui-col-sm-4">
                                <a href="#">
                                    <span class="mui-icon mui-icon-phone"></span>
                                    <div class="mui-media-body">Phone</div>
                                </a>
                            </li>
                            <li class="mui-table-view-cell mui-media mui-col-xs-4 mui-col-sm-4">
                                <a href="#">
                                    <span class="mui-icon mui-icon-gear"></span>
                                    <div class="mui-media-body">Setting</div>
                                </a>
                            </li>
                            <li class="mui-table-view-cell mui-media mui-col-xs-4 mui-col-sm-4">
                                <a href="#">
                                    <span class="mui-icon mui-icon-info"></span>
                                    <div class="mui-media-body">about</div>
                                </a>
                            </li>
                            <li class="mui-table-view-cell mui-media mui-col-xs-4 mui-col-sm-4">
                                <a href="#">
                                    <span class="mui-icon mui-icon-more"></span>
                                    <div class="mui-media-body">more</div>
                                </a>
                            </li>
                        </ul>
                    </div>
                    <div class="mui-slider-item">
                        <ul class="mui-table-view mui-grid-view mui-grid-9">
                            <li class="mui-table-view-cell mui-media mui-col-xs-4 mui-col-sm-4">
                                <a href="#">
                                    <span class="mui-icon mui-icon-home"></span>
                                    <div class="mui-media-body">Home</div>
                                </a>
                            </li>
                            <li class="mui-table-view-cell mui-media mui-col-xs-4 mui-col-sm-4">
                                <a href="#">
                                    <span class="mui-icon mui-icon-email"><span class="mui-badge">5</span></span>
                                    <div class="mui-media-body">Email</div>
                                </a>
                            </li>
                            <li class="mui-table-view-cell mui-media mui-col-xs-4 mui-col-sm-4">
                                <a href="#">
                                    <span class="mui-icon mui-icon-chatbubble"></span>
                                    <div class="mui-media-body">Chat</div>
                                </a>
                            </li>
                            <li class="mui-table-view-cell mui-media mui-col-xs-4 mui-col-sm-4">
                                <a href="#">
                                    <span class="mui-icon mui-icon-location"></span>
                                    <div class="mui-media-body">location</div>
                                </a>
                            </li>
                            <li class="mui-table-view-cell mui-media mui-col-xs-4 mui-col-sm-4">
                                <a href="#">
                                    <span class="mui-icon mui-icon-search"></span>
                                    <div class="mui-media-body">Search</div>
                                </a>
                            </li>
                            <li class="mui-table-view-cell mui-media mui-col-xs-4 mui-col-sm-4">
                                <a href="#">
                                    <span class="mui-icon mui-icon-phone"></span>
                                    <div class="mui-media-body">Phone</div>
                                </a>
                            </li>
                            <li class="mui-table-view-cell mui-media mui-col-xs-4 mui-col-sm-4">
                                <a href="#">
                                    <span class="mui-icon mui-icon-gear"></span>
                                    <div class="mui-media-body">Setting</div>
                                </a>
                            </li>
                            <li class="mui-table-view-cell mui-media mui-col-xs-4 mui-col-sm-4">
                                <a href="#">
                                    <span class="mui-icon mui-icon-info"></span>
                                    <div class="mui-media-body">about</div>
                                </a>
                            </li>
                            <li class="mui-table-view-cell mui-media mui-col-xs-4 mui-col-sm-4">
                                <a href="#">
                                    <span class="mui-icon mui-icon-more"></span>
                                    <div class="mui-media-body">more</div>
                                </a>
                            </li>
                        </ul>
                    </div>
                    <div class="mui-slider-item">
                        <ul class="mui-table-view mui-grid-view mui-grid-9">
                            <li class="mui-table-view-cell mui-media mui-col-xs-4 mui-col-sm-4">
                                <a href="#">
                                    <span class="mui-icon mui-icon-home"></span>
                                    <div class="mui-media-body">Home</div>
                                </a>
                            </li>
                            <li class="mui-table-view-cell mui-media mui-col-xs-4 mui-col-sm-4">
                                <a href="#">
                                    <span class="mui-icon mui-icon-email"><span class="mui-badge">5</span></span>
                                    <div class="mui-media-body">Email</div>
                                </a>
                            </li>
                            <li class="mui-table-view-cell mui-media mui-col-xs-4 mui-col-sm-4">
                                <a href="#">
                                    <span class="mui-icon mui-icon-chatbubble"></span>
                                    <div class="mui-media-body">Chat</div>
                                </a>
                            </li>
                            <li class="mui-table-view-cell mui-media mui-col-xs-4 mui-col-sm-4">
                                <a href="#">
                                    <span class="mui-icon mui-icon-location"></span>
                                    <div class="mui-media-body">location</div>
                                </a>
                            </li>
                            <li class="mui-table-view-cell mui-media mui-col-xs-4 mui-col-sm-4">
                                <a href="#">
                                    <span class="mui-icon mui-icon-search"></span>
                                    <div class="mui-media-body">Search</div>
                                </a>
                            </li>
                            <li class="mui-table-view-cell mui-media mui-col-xs-4 mui-col-sm-4">
                                <a href="#">
                                    <span class="mui-icon mui-icon-phone"></span>
                                    <div class="mui-media-body">Phone</div>
                                </a>
                            </li>
                            <li class="mui-table-view-cell mui-media mui-col-xs-4 mui-col-sm-4">
                                <a href="#">
                                    <span class="mui-icon mui-icon-gear"></span>
                                    <div class="mui-media-body">Setting</div>
                                </a>
                            </li>
                            <li class="mui-table-view-cell mui-media mui-col-xs-4 mui-col-sm-4">
                                <a href="#">
                                    <span class="mui-icon mui-icon-info"></span>
                                    <div class="mui-media-body">about</div>
                                </a>
                            </li>
                            <li class="mui-table-view-cell mui-media mui-col-xs-4 mui-col-sm-4">
                                <a href="#">
                                    <span class="mui-icon mui-icon-more"></span>
                                    <div class="mui-media-body">more</div>
                                </a>
                            </li>
                        </ul>
                    </div>

                </div>
                <div class="mui-slider-indicator">
                    <div class="mui-indicator mui-active"></div>
                    <div class="mui-indicator"></div>
                    <div class="mui-indicator"></div>
                </div>
            </div>

        </nav>




        <script src="../js/mui.min.js"></script>
        <script type="text/javascript" src="../js/jquery-1.11.0.min.js" ></script>
        <script type="text/javascript">
            mui.init();

            //mui加载事件
            mui.plusReady(function(){
                //获取当前webView
                var self = plus.webview.currentWebview();
                //获取传递过来的数据
                var title = self.title;
                //设置好友名称
                document.querySelector("#title").innerText=title;
            });
        </script>
    </body>

</html>
```



## 聊天实现发送文本

### 实现步骤

1. 了解页面发送文本数据样式，在代码注释里面有自己发送文本信息样式模板代码
2. 给发送文本数据图表注册轻击事件，在事件里面获取文本框的value和结合上面模板代码进行发送消息拼接html代码

### 实现代码

```javascript
<script src="../js/mui.min.js"></script>
<script type="text/javascript" src="../js/jquery-1.11.0.min.js" ></script>
<script type="text/javascript">
    mui.init();

//mui加载事件
mui.plusReady(function(){
    //获取当前webView
    var self = plus.webview.currentWebview();
    //获取传递过来的数据
    var title = self.title;
    //设置好友名称
    document.querySelector("#title").innerText=title;


    //获取发送图标对象
    var sendNode = document.getElementById("msg-type");
    //注册轻击事件
    sendNode.addEventListener("tap",function(){
        //文本框的值
        var msgValue = $("#msg-text").val();
        //如果文本为空就不发送，否则才发送消息
        if(msgValue){
            $("#msg-list").append("<div class=\"msg-item msg-item-self msg-content\">"+
                                  "<img class=\"msg-user-img\" src=\"../img/2.jpg\" style=\"float:right\" />"+
                                  "<div class=\"msg-content\">"+
                                  "<div class=\"msg-content-inner\">"+msgValue+

                                  "</div>"+
                                  "<div class=\"msg-content-arrow\"></div>"+
                                  "</div>"+
                                  "<div class=\"mui-item-clear\"></div></div>");
        }
        //清空消息
        $("#msg-text").val("");
    });

});

</script>
```



## 聊天实现打开相册发送图片

### 实现步骤

1. 在页面底部增加九宫格mui组件，并设置dispay默认不显示样式

   ```html
   <!--底部发送消息内容-->
   <nav class="mui-bar mui-bar-tab" style="padding-top: 15px;">
       <i id='msg-image' class="mui-icon mui-icon-plus" style="font-size: 28px;float:left;width:15%;padding-left:10px;"></i>
       <textarea id='msg-text' type="text" class='input-text' style="float:left;width:70%;height:50px;border-radius:10px;"></textarea>
       <i id='msg-type' class="mui-icon mui-icon-paperplane" style="float:left;width:15%;padding-left:10px;"></i>

       <!--九宫格内容-->
       <div id="Gallery" class="mui-slider" style="margin-top:15px;display: none;">
           ...
       </div>
   </nav>
   ```

   使用快捷键快速加入九宫格

   ![](img/24.png)

2. 点击加号显示九宫格mui组件，再次点击就隐藏九宫格

   ```javascript
   //获取加号对象
   var jiaNode = document.getElementById("msg-image");
   //注册tap轻击事件
   jiaNode.addEventListener("tap",function(){
       //获取九宫格显示属性值
       var dispayValue = document.getElementById("Gallery").style.display;
       //判断，如果隐藏就显示，显示就隐藏
       if(dispayValue && dispayValue=="none"){
           document.getElementById("Gallery").style.display="block";
       }else{
           document.getElementById("Gallery").style.display="none";
       }
   });
   ```

3. 九宫格中第一个Home替换成相册，一会用于打开硬件相册发送图片

   ```html
   <li id="galleryID" class="mui-table-view-cell mui-media mui-col-xs-4 mui-col-sm-4">
   <a href="#">
   <span class="mui-icon mui-icon-image"></span>
   <div class="mui-media-body">相册</div>
   </a>
   </li>
   ```

4. 给相册注册tap轻击事件，打开系统硬件相册选取图片,将选取返回的图片路径拼接html追加到聊天消息页面内

   ```javascript
   //获取相册按钮对象
   var gallery = $("#galleryID")[0];
   //给相册注册轻击事件
   gallery.addEventListener("tap",function(){
   //调用硬件相册并返回选择的图片的路径
   //plus.gallery.pick(function(path){});一个参数时，选择图片为单选，只能选择一张
   //多选图片如下
   plus.gallery.pick(function(e){
   //e,返回多张图片地址的数组，e.files就是数组
   for(var i in e.files){
   //将图片根据发送图片格式拼接html，追加到聊天消息内
   //$("#msg-list").append(e.files[i]);	
   $("#msg-list").append("<div class=\"msg-item msg-item-self msg-type msg-content\">"+

   "<img class=\"msg-user-img\" src=\"../img/2.jpg\" alt=\"\" style=\"float: right;\" />"+

   "<div class=\"msg-content\">"+
   "<div class=\"msg-content-inner\">"+

   "<img class=\"msg-content-image\" src=\""+e.files[i]+"\" style=\"max-width: 100px;\" />"+

   "</div>"+
   "<div class=\"msg-content-arrow\"></div>"+
   "</div>"+
   "<div class=\"mui-item-clear\"></div></div>");
   }
   //清空换行
   $("br").remove();
   $("#msg-list").append("<br/><br/>");

   },function(){},{filter:"image",multiple:true});
   //隐藏九宫格
   document.getElementById("Gallery").style.display="none";
   });
   ```

### 实现代码

chat.html完整页面代码

```html
<!DOCTYPE html>
<html>

	<head>
		<meta charset="utf-8">
		<meta name="viewport" content="width=device-width,initial-scale=1,minimum-scale=1,maximum-scale=1,user-scalable=no" />
		<title></title>
		<link href="../css/mui.min.css" rel="stylesheet" />
		<style>
			/*
 *这是单独为hello mui准备的个性化css，可以覆盖标准mui的css定义；
 * 在实际项目开发时，建议为App单独写一个css文件，从而实现项目的自定义皮肤功能；
 * 
 * */
			
			.mui-plus.mui-android header.mui-bar {
				float: left;
			}
			
			.mui-plus.mui-android .mui-bar-nav~.mui-content {
				padding-top: 41px;
			}
			
			.mui-active .mui-icon,
			.mui-tab-label {
				color: #45C018;
			}
			/*hm开头的表示仅为 Hello MUI示例定义*/
			
			.hm-description {
				margin: .5em 0;
			}
			
			.hm-description>li {
				font-size: 14px;
				color: #8f8f94;
			}
			
			.mui-bar-nav {
				background: #393a3e;
			}
			
			.mui-icon-arrowthinleft,
			.mui-pull-left,
			.mui-pull-right {
				color: white;
			}
			
			.mui-icon-mic {
				padding-left: 5px;
				float: left;
			}
			
			html,
			body {
				height: 100%;
				overflow: hidden;
			}
			
			.mui-bar {
				-webkit-box-shadow: none;
				box-shadow: none;
			}
			
			.faxianListMedia {
				height: 30px;
				line-height: 30px;
				overflow: hidden;
				float: left;
				padding-left: 15px;
			}
			
			.faxianImage {
				width: 30px;
				height: 30px;
				float: left;
			}
			
			html,
			body {
				height: 100%;
				margin: 0px;
				padding: 0px;
				overflow: hidden;
				-webkit-touch-callout: none;
				-webkit-user-select: none;
			}
			
			footer {
				position: fixed;
				width: 100%;
				height: 50px;
				min-height: 50px;
				border-top: solid 1px #bbb;
				left: 0px;
				bottom: 0px;
				overflow: hidden;
				padding: 0px 50px;
				background-color: #fafafa;
			}
			
			.footer-left {
				position: absolute;
				width: 50px;
				height: 50px;
				left: 0px;
				/*bottom: 0px;*/
				text-align: center;
				vertical-align: middle;
				line-height: 100%;
				padding: 12px 4px;
			}
			
			.footer-right {
				position: absolute;
				width: 50px;
				height: 50px;
				right: 0px;
				bottom: 0px;
				text-align: center;
				vertical-align: middle;
				line-height: 100%;
				padding: 12px 5px;
				display: inline-block;
			}
			
			.footer-center {
				height: 100%;
				padding: 5px 0px;
			}
			
			.footer-center [class*=input] {
				width: 100%;
				height: 100%;
				border-radius: 5px;
			}
			
			.footer-center .input-text {
				background: #fff;
				border: solid 1px #ddd;
				padding: 10px !important;
				font-size: 16px !important;
				line-height: 18px !important;
				font-family: verdana !important;
				overflow: hidden;
			}
			
			.footer-center .input-sound {
				background-color: #eee;
			}
			
			.mui-content {
				height: 100%;
				padding: 44px 0px 50px 0px;
				overflow: auto;
				background-color: #eaeaea;
			}
			
			#msg-list {
				height: 100%;
				overflow: auto;
				-webkit-overflow-scrolling: touch;
			}
			
			.msg-item {
				padding: 8px;
				clear: both;
			}
			
			.msg-item .mui-item-clear {
				clear: both;
			}
			
			.msg-item .msg-user {
				width: 38px;
				height: 38px;
				border: solid 1px #d3d3d3;
				display: inline-block;
				background: #fff;
				border-radius: 3px;
				vertical-align: top;
				text-align: center;
				float: left;
				padding: 3px;
				color: #ddd;
			}
			
			.msg-item .msg-user-img {
				width: 38px;
				height: 38px;
				display: inline-block;
				border-radius: 3px;
				vertical-align: top;
				text-align: center;
				float: left;
				color: #ddd;
			}
			
			.msg-item .msg-content {
				display: inline-block;
				border-radius: 5px;
				border: solid 1px #d3d3d3;
				background-color: #FFFFFF;
				color: #333;
				padding: 8px;
				vertical-align: top;
				font-size: 15px;
				position: relative;
				margin: 0px 8px;
				max-width: 75%;
				min-width: 35px;
				float: left;
			}
			
			.msg-item .msg-content .msg-content-inner {
				overflow-x: hidden;
			}
			
			.msg-item .msg-content .msg-content-arrow {
				position: absolute;
				border: solid 1px #d3d3d3;
				border-right: none;
				border-top: none;
				background-color: #FFFFFF;
				width: 10px;
				height: 10px;
				left: -5px;
				top: 12px;
				-webkit-transform: rotateZ(45deg);
				transform: rotateZ(45deg);
			}
			
			.msg-item-self .msg-user,
			.msg-item-self .msg-content {
				float: right;
			}
			
			.msg-item-self .msg-content .msg-content-arrow {
				left: auto;
				right: -5px;
				-webkit-transform: rotateZ(225deg);
				transform: rotateZ(225deg);
			}
			
			.msg-item-self .msg-content,
			.msg-item-self .msg-content .msg-content-arrow {
				background-color: #4CD964;
				color: #fff;
				border-color: #2AC845;
			}
			
			footer .mui-icon {
				color: #000;
			}
			
			footer .mui-icon:active {
				color: #007AFF !important;
			}
			
			footer .mui-icon-paperplane:before {
				content: "发送";
			}
			
			footer .mui-icon-paperplane {
				/*-webkit-transform: rotateZ(45deg);
				transform: rotateZ(45deg);*/
				font-size: 16px;
				word-break: keep-all;
				line-height: 100%;
				padding-top: 6px;
				color: rgba(0, 135, 250, 1);
			}
			
			#msg-sound {
				-webkit-user-select: none !important;
				user-select: none !important;
			}
			
			.rprogress {
				position: absolute;
				left: 50%;
				top: 50%;
				width: 140px;
				height: 140px;
				margin-left: -70px;
				margin-top: -70px;
				background-image: url(../images/arecord.png);
				background-repeat: no-repeat;
				background-position: center center;
				background-size: 30px 30px;
				background-color: rgba(0, 0, 0, 0.7);
				border-radius: 5px;
				display: none;
				-webkit-transition: .15s;
			}
			
			.rschedule {
				background-color: rgba(0, 0, 0, 0);
				border: 5px solid rgba(0, 183, 229, 0.9);
				opacity: .9;
				border-left: 5px solid rgba(0, 0, 0, 0);
				border-right: 5px solid rgba(0, 0, 0, 0);
				border-radius: 50px;
				box-shadow: 0 0 15px #2187e7;
				width: 46px;
				height: 46px;
				position: absolute;
				left: 50%;
				top: 50%;
				margin-left: -23px;
				margin-top: -23px;
				-webkit-animation: spin 1s infinite linear;
				animation: spin 1s infinite linear;
			}
			
			.r-sigh {
				display: none;
				border-radius: 50px;
				box-shadow: 0 0 15px #2187e7;
				width: 46px;
				height: 46px;
				position: absolute;
				left: 50%;
				top: 50%;
				margin-left: -23px;
				margin-top: -23px;
				text-align: center;
				line-height: 46px;
				font-size: 40px;
				font-weight: bold;
				color: #2187e7;
			}
			
			.rprogress-sigh {
				background-image: none !important;
			}
			
			.rprogress-sigh .rschedule {
				display: none !important;
			}
			
			.rprogress-sigh .r-sigh {
				display: block !important;
			}
			
			.rsalert {
				font-size: 12px;
				color: #bbb;
				text-align: center;
				position: absolute;
				border-radius: 5px;
				width: 130px;
				margin: 5px 5px;
				padding: 5px;
				left: 0px;
				bottom: 0px;
			}
			
			@-webkit-keyframes spin {
				0% {
					-webkit-transform: rotate(0deg);
				}
				100% {
					-webkit-transform: rotate(360deg);
				}
			}
			
			@keyframes spin {
				0% {
					transform: rotate(0deg);
				}
				100% {
					transform: rotate(360deg);
				}
			}
			
			#h {
				background: #fff;
				border: solid 1px #ddd;
				padding: 10px !important;
				font-size: 16px !important;
				font-family: verdana !important;
				line-height: 18px !important;
				overflow: visible;
				position: absolute;
				left: -1000px;
				right: 0px;
				word-break: break-all;
				word-wrap: break-word;
			}
			
			.cancel {
				background-color: darkred;
			}
			.mui-bar-tab{display:inline;height:auto;}
		</style>
		<link rel="stylesheet" type="text/css" href="css/main.css" />
	</head>

	<body contextmenu="return false;">
		<header class="mui-bar mui-bar-nav">
			<a class="mui-action-back mui-icon mui-icon-left-nav mui-pull-left" id="title"></a>
		</header>
		<pre id='h'></pre>

		<div class="mui-content">
			<div id='msg-list'>
				<!--好友发送图片格式-->
				<div class="msg-item 1msg-item-self1 msg-type msg-content">

					<img class="msg-user-img" src="../img/1.jpg" alt="" />

					<div class="msg-content">
						<div class="msg-content-inner">

							<img class="msg-content-image" src="../img/4.jpg" style="max-width: 100px;" />

						</div>
						<div class="msg-content-arrow"></div>
					</div>
					<div class="mui-item-clear"></div>
				</div>
				<!--好友的文本格式-->
				<div class="msg-item msg-item-self1 msg-type msg-content">
					<img class="msg-user-img" src="../img/1.jpg" alt="" />
					<div class="msg-content">
						<div class="msg-content-inner">
							你好
						</div>
						<div class="msg-content-arrow"></div>
					</div>
					<div class="mui-item-clear"></div>
				</div>
				<!--自己的文本格式
				<div class="msg-item msg-item-self msg-content">
					<img class="msg-user-img" src="../img/2.jpg" style="float:right" />
					<div class="msg-content">
						<div class="msg-content-inner">
							你好
						</div>
						<div class="msg-content-arrow"></div>
					</div>
					<div class="mui-item-clear"></div>
				</div>
				-->
				
				<!--自己发送图片格式
				<div class="msg-item msg-item-self msg-type msg-content">

					<img class="msg-user-img" src="../img/2.jpg" alt="" style="float: right;" />

					<div class="msg-content">
						<div class="msg-content-inner">

							<img class="msg-content-image" src="../img/4.jpg" style="max-width: 100px;" />

						</div>
						<div class="msg-content-arrow"></div>
					</div>
					<div class="mui-item-clear"></div>
				</div>
				-->
			</div>
			

			
			
			
		</div>
	
		<!--底部发送消息内容-->
		<nav class="mui-bar mui-bar-tab" style="padding-top: 15px;">
		    <i id='msg-image' class="mui-icon mui-icon-plus" style="font-size: 28px;float:left;width:15%;padding-left:10px;"></i>
		    <textarea id='msg-text' type="text" class='input-text' style="float:left;width:70%;height:50px;border-radius:10px;"></textarea>
		    <i id='msg-type' class="mui-icon mui-icon-paperplane" style="float:left;width:15%;padding-left:10px;"></i>
			
			<!--九宫格内容-->
			<div id="Gallery" class="mui-slider" style="margin-top:15px;display: none;">
				<div class="mui-slider-group">
					<div class="mui-slider-item">
						<ul class="mui-table-view mui-grid-view mui-grid-9">
							<li id="galleryID" class="mui-table-view-cell mui-media mui-col-xs-4 mui-col-sm-4">
								<a href="#">
									<span class="mui-icon mui-icon-image"></span>
									<div class="mui-media-body">相册</div>
								</a>
							</li>
							<li class="mui-table-view-cell mui-media mui-col-xs-4 mui-col-sm-4">
								<a href="#">
									<span class="mui-icon mui-icon-email"><span class="mui-badge">5</span></span>
									<div class="mui-media-body">Email</div>
								</a>
							</li>
							<li class="mui-table-view-cell mui-media mui-col-xs-4 mui-col-sm-4">
								<a href="#">
									<span class="mui-icon mui-icon-chatbubble"></span>
									<div class="mui-media-body">Chat</div>
								</a>
							</li>
							<li class="mui-table-view-cell mui-media mui-col-xs-4 mui-col-sm-4">
								<a href="#">
									<span class="mui-icon mui-icon-location"></span>
									<div class="mui-media-body">location</div>
								</a>
							</li>
							<li class="mui-table-view-cell mui-media mui-col-xs-4 mui-col-sm-4">
								<a href="#">
									<span class="mui-icon mui-icon-search"></span>
									<div class="mui-media-body">Search</div>
								</a>
							</li>
							<li class="mui-table-view-cell mui-media mui-col-xs-4 mui-col-sm-4">
								<a href="#">
									<span class="mui-icon mui-icon-phone"></span>
									<div class="mui-media-body">Phone</div>
								</a>
							</li>
							<li class="mui-table-view-cell mui-media mui-col-xs-4 mui-col-sm-4">
								<a href="#">
									<span class="mui-icon mui-icon-gear"></span>
									<div class="mui-media-body">Setting</div>
								</a>
							</li>
							<li class="mui-table-view-cell mui-media mui-col-xs-4 mui-col-sm-4">
								<a href="#">
									<span class="mui-icon mui-icon-info"></span>
									<div class="mui-media-body">about</div>
								</a>
							</li>
							<li class="mui-table-view-cell mui-media mui-col-xs-4 mui-col-sm-4">
								<a href="#">
									<span class="mui-icon mui-icon-more"></span>
									<div class="mui-media-body">more</div>
								</a>
							</li>
						</ul>
					</div>
					<div class="mui-slider-item">
						<ul class="mui-table-view mui-grid-view mui-grid-9">
							<li class="mui-table-view-cell mui-media mui-col-xs-4 mui-col-sm-4">
								<a href="#">
									<span class="mui-icon mui-icon-home"></span>
									<div class="mui-media-body">Home</div>
								</a>
							</li>
							<li class="mui-table-view-cell mui-media mui-col-xs-4 mui-col-sm-4">
								<a href="#">
									<span class="mui-icon mui-icon-email"><span class="mui-badge">5</span></span>
									<div class="mui-media-body">Email</div>
								</a>
							</li>
							<li class="mui-table-view-cell mui-media mui-col-xs-4 mui-col-sm-4">
								<a href="#">
									<span class="mui-icon mui-icon-chatbubble"></span>
									<div class="mui-media-body">Chat</div>
								</a>
							</li>
							<li class="mui-table-view-cell mui-media mui-col-xs-4 mui-col-sm-4">
								<a href="#">
									<span class="mui-icon mui-icon-location"></span>
									<div class="mui-media-body">location</div>
								</a>
							</li>
							<li class="mui-table-view-cell mui-media mui-col-xs-4 mui-col-sm-4">
								<a href="#">
									<span class="mui-icon mui-icon-search"></span>
									<div class="mui-media-body">Search</div>
								</a>
							</li>
							<li class="mui-table-view-cell mui-media mui-col-xs-4 mui-col-sm-4">
								<a href="#">
									<span class="mui-icon mui-icon-phone"></span>
									<div class="mui-media-body">Phone</div>
								</a>
							</li>
							<li class="mui-table-view-cell mui-media mui-col-xs-4 mui-col-sm-4">
								<a href="#">
									<span class="mui-icon mui-icon-gear"></span>
									<div class="mui-media-body">Setting</div>
								</a>
							</li>
							<li class="mui-table-view-cell mui-media mui-col-xs-4 mui-col-sm-4">
								<a href="#">
									<span class="mui-icon mui-icon-info"></span>
									<div class="mui-media-body">about</div>
								</a>
							</li>
							<li class="mui-table-view-cell mui-media mui-col-xs-4 mui-col-sm-4">
								<a href="#">
									<span class="mui-icon mui-icon-more"></span>
									<div class="mui-media-body">more</div>
								</a>
							</li>
						</ul>
					</div>
					<div class="mui-slider-item">
						<ul class="mui-table-view mui-grid-view mui-grid-9">
							<li class="mui-table-view-cell mui-media mui-col-xs-4 mui-col-sm-4">
								<a href="#">
									<span class="mui-icon mui-icon-home"></span>
									<div class="mui-media-body">Home</div>
								</a>
							</li>
							<li class="mui-table-view-cell mui-media mui-col-xs-4 mui-col-sm-4">
								<a href="#">
									<span class="mui-icon mui-icon-email"><span class="mui-badge">5</span></span>
									<div class="mui-media-body">Email</div>
								</a>
							</li>
							<li class="mui-table-view-cell mui-media mui-col-xs-4 mui-col-sm-4">
								<a href="#">
									<span class="mui-icon mui-icon-chatbubble"></span>
									<div class="mui-media-body">Chat</div>
								</a>
							</li>
							<li class="mui-table-view-cell mui-media mui-col-xs-4 mui-col-sm-4">
								<a href="#">
									<span class="mui-icon mui-icon-location"></span>
									<div class="mui-media-body">location</div>
								</a>
							</li>
							<li class="mui-table-view-cell mui-media mui-col-xs-4 mui-col-sm-4">
								<a href="#">
									<span class="mui-icon mui-icon-search"></span>
									<div class="mui-media-body">Search</div>
								</a>
							</li>
							<li class="mui-table-view-cell mui-media mui-col-xs-4 mui-col-sm-4">
								<a href="#">
									<span class="mui-icon mui-icon-phone"></span>
									<div class="mui-media-body">Phone</div>
								</a>
							</li>
							<li class="mui-table-view-cell mui-media mui-col-xs-4 mui-col-sm-4">
								<a href="#">
									<span class="mui-icon mui-icon-gear"></span>
									<div class="mui-media-body">Setting</div>
								</a>
							</li>
							<li class="mui-table-view-cell mui-media mui-col-xs-4 mui-col-sm-4">
								<a href="#">
									<span class="mui-icon mui-icon-info"></span>
									<div class="mui-media-body">about</div>
								</a>
							</li>
							<li class="mui-table-view-cell mui-media mui-col-xs-4 mui-col-sm-4">
								<a href="#">
									<span class="mui-icon mui-icon-more"></span>
									<div class="mui-media-body">more</div>
								</a>
							</li>
						</ul>
					</div>

				</div>
				<div class="mui-slider-indicator">
					<div class="mui-indicator mui-active"></div>
					<div class="mui-indicator"></div>
					<div class="mui-indicator"></div>
				</div>
			</div>
			
		</nav>
		
		<script src="../js/mui.min.js"></script>
		<script type="text/javascript" src="../js/jquery-1.11.0.min.js" ></script>
		<script type="text/javascript">
			mui.init();
			
			//mui加载事件
			mui.plusReady(function(){
				//获取当前webView
				var self = plus.webview.currentWebview();
				//获取传递过来的数据
				var title = self.title;
				//设置好友名称
				document.querySelector("#title").innerText=title;
				
				//获取加号对象
				var jiaNode = document.getElementById("msg-image");
				//注册tap轻击事件
				jiaNode.addEventListener("tap",function(){
					//获取九宫格显示属性值
					var dispayValue = document.getElementById("Gallery").style.display;
					//判断，如果隐藏就显示，显示就隐藏
					if(dispayValue && dispayValue=="none"){
						document.getElementById("Gallery").style.display="block";
					}else{
						document.getElementById("Gallery").style.display="none";
					}
				});
				
				//获取发送图标对象
				var sendNode = document.getElementById("msg-type");
				//注册轻击事件
				sendNode.addEventListener("tap",function(){
					//文本框的值
					var msgValue = $("#msg-text").val();
					//如果文本为空就不发送，否则才发送消息
					if(msgValue){
						$("#msg-list").append("<div class=\"msg-item msg-item-self msg-content\">"+
					"<img class=\"msg-user-img\" src=\"../img/2.jpg\" style=\"float:right\" />"+
					"<div class=\"msg-content\">"+
						"<div class=\"msg-content-inner\">"+msgValue+
							
						"</div>"+
						"<div class=\"msg-content-arrow\"></div>"+
					"</div>"+
					"<div class=\"mui-item-clear\"></div></div>");
					}
					//清空消息
					$("#msg-text").val("");
					$("br").remove();
					$("#msg-list").append("<br/><br/>");
				});
				
				//获取相册按钮对象
				var gallery = $("#galleryID")[0];
				//给相册注册轻击事件
				gallery.addEventListener("tap",function(){
					//调用硬件相册并返回选择的图片的路径
					//plus.gallery.pick(function(path){});一个参数时，选择图片为单选，只能选择一张
					//多选图片如下
					plus.gallery.pick(function(e){
						//e,返回多张图片地址的数组，e.files就是数组
						for(var i in e.files){
							//将图片根据发送图片格式拼接html，追加到聊天消息内
							//$("#msg-list").append(e.files[i]);	
							$("#msg-list").append("<div class=\"msg-item msg-item-self msg-type msg-content\">"+

					"<img class=\"msg-user-img\" src=\"../img/2.jpg\" alt=\"\" style=\"float: right;\" />"+

					"<div class=\"msg-content\">"+
						"<div class=\"msg-content-inner\">"+

							"<img class=\"msg-content-image\" src=\""+e.files[i]+"\" style=\"max-width: 100px;\" />"+

						"</div>"+
						"<div class=\"msg-content-arrow\"></div>"+
					"</div>"+
					"<div class=\"mui-item-clear\"></div></div>");
						}
					//清空换行
					$("br").remove();
					$("#msg-list").append("<br/><br/>");
						
					},function(){},{filter:"image",multiple:true});
					//隐藏九宫格
					document.getElementById("Gallery").style.display="none";
					
					
				});
				

			});
			
		</script>
	</body>

</html>
```

# 微信导航发现页面布局

## 效果

![](img/25.png)

## 实现分析

浏览mui所有组件，会发现list列表组件非常适合这个页面布局

## 完整代码

sub3.html页面代码

```html
<!doctype html>
<html>

    <head>
        <meta charset="UTF-8">
        <title></title>
        <meta name="viewport" content="width=device-width,initial-scale=1,minimum-scale=1,maximum-scale=1,user-scalable=no" />
        <link href="css/mui.min.css" rel="stylesheet" />
        <style type="text/css">
            .mui-table-view-cell{
                font-size: 18px; 
                line-height: 30px;
            }
        </style>
    </head>

    <body>
        <script src="js/mui.min.js"></script>
        <script type="text/javascript">
            mui.init()
        </script>
        <div class="mui-content">
            <ul class="mui-table-view">
                <li class="mui-table-view-cell" ><img src="img/afp.png" width="30px" height="30px" align="absmiddle">&nbsp;&nbsp;朋友圈</li>
            </ul>
            <br>
            <ul class="mui-table-view">
                <li class="mui-table-view-cell"><img src="img/afs.png" width="30px" height="30px" align="absmiddle">&nbsp;&nbsp;扫一扫</li>
                <li class="mui-table-view-cell"><img src="img/afy.png" width="30px" height="30px" align="absmiddle">&nbsp;&nbsp;摇一摇</li>
            </ul>
            <br>
            <ul class="mui-table-view">
                <li class="mui-table-view-cell"><img src="img/afg.png" width="30px" height="30px" align="absmiddle">&nbsp;&nbsp;购物</li>
                <li class="mui-table-view-cell"><img src="img/afyx.png" width="30px" height="30px" align="absmiddle">&nbsp;&nbsp;游戏</li>
            </ul>

        </div>
    </body>

</html>
```



# 朋友圈实现上拉刷新和下拉加载

## 效果

打开朋友圈页面效果

![](img/26.png)

上拉刷新和下拉加载效果

![](img/27.png)

## 上拉刷新和下拉加载

### 实现分析

利用mui提供上拉刷新和下拉加载组件示例完成功能

组件代码

```
<!--上拉和下拉刷新容器-->
<div id="pullrefresh" class="mui-content mui-scroll-wrapper">
	<div class="mui-scroll">
	  //自己的数据和html布局代码
	</div>
</div>
```

只要将自己布局的数据放入到上拉和下拉刷新容器中，用户就可以在手机界面进行上拉和下拉的动作，之后设置上拉和下拉的动作回调函数

```javascript
<script type="text/javascript">
//mui初始化配置上拉和刷新的回调函数
mui.init({
    pullRefresh: {
        container: '#pullrefresh',
        down: {
            style:'circle',
            callback: pulldownRefresh
        },
        up: {
        	callback: pullupRefresh
        }
    }
});

//下拉
function pulldownRefresh(){
//执行动作对应的命令
}
//上拉
function pullupRefresh(){
//执行动作对应的命令

}
</script>
```

### 实现代码

```html
<!doctype html>
<html>

	<head>
		<meta charset="UTF-8">
		<title></title>
		<meta name="viewport" content="width=device-width,initial-scale=1,minimum-scale=1,maximum-scale=1,user-scalable=no" />
		<link href="../css/mui.min.css" rel="stylesheet" />
	</head>

	<body>
	<!--下拉刷新容器-->
		<div id="pullrefresh" class="mui-content mui-scroll-wrapper">
			<div class="mui-scroll">
				<div style="position: relative">
					<div style="">
						<a href="#">
							<img height="250px" width="100%" src="../img/1.jpg">
						</a>
					</div>
					<div style="float: right;padding-right: 10px;margin-top: -55px;z-index: 2;position: relative;">
						<div style="float: left;padding-top: 25px; padding-right: 10px;color: white;">
							<b>我的微信</b>
						</div>
						<div style="float: left;">
							<a href="#">
								<img height="80px" width="80px" src="../img/2.jpg" style="border: 2px solid white;" />
							</a>
						</div>
					</div>
				</div>
				<div id="popover" class="mui-popover" style="width: 100px;">
					<ul class="mui-table-view">
						<li class="mui-table-view-cell">
							<a href="#"><span class="mui-icon mui-icon-star"></span>赞</a>
						</li>
						<li class="mui-table-view-cell">
							<a href="#"><span class="mui-icon mui-icon-chatbubble"></span>评论</a>
						</li>
					</ul>
				</div>
				<div id="dataList" style="margin-top:-5px;padding-top: 35px;background: white;" class="data">
					<ul class="mui-table-view">
						<li class="mui-table-view-cell mui-media" style="width: 100%;">
							<img class="mui-media-object mui-pull-left" src="../img/3.jpg">
							<div class="mui-media-body" style="">
								<font color="#2187E7">幸福</font><br /> 能和心爱的人一起睡觉，是件幸福的事情；可是，打呼噜怎么办？<br />
								<div>
									<p style="font-size: 13px;padding-top: 5px;float: left;">18分钟前</p>
									<a href="#popover" id="openPopover" class="mui-icon mui-icon-compose" style="float: right;"></a>
								</div>
							</div>
						</li>
					</ul>
					<ul class="mui-table-view">
						<li class="mui-table-view-cell mui-media" style="width: 100%;">
							<img class="mui-media-object mui-pull-left" src="../img/3.jpg">
							<div class="mui-media-body" style="">
								<font color="#2187E7">幸福</font><br /> 能和心爱的人一起睡觉，是件幸福的事情；可是，打呼噜怎么办？<br />
								<div>
									<p style="font-size: 13px;padding-top: 5px;float: left;">18分钟前</p>
									<a href="#popover" id="openPopover" class="mui-icon mui-icon-compose" style="float: right;"></a>
								</div>
							</div>
						</li>
					</ul>
					<ul class="mui-table-view">
						<li class="mui-table-view-cell mui-media" style="width: 100%;">
							<img class="mui-media-object mui-pull-left" src="../img/3.jpg">
							<div class="mui-media-body" style="">
								<font color="#2187E7">幸福</font><br /> 能和心爱的人一起睡觉，是件幸福的事情；可是，打呼噜怎么办？<br />
								<div>
									<p style="font-size: 13px;padding-top: 5px;float: left;">18分钟前</p>
									<a href="#popover" id="openPopover" class="mui-icon mui-icon-compose" style="float: right;"></a>
								</div>
							</div>
						</li>
					</ul>
					<ul class="mui-table-view">
						<li class="mui-table-view-cell mui-media" style="width: 100%;">
							<img class="mui-media-object mui-pull-left" src="../img/3.jpg">
							<div class="mui-media-body" style="">
								<font color="#2187E7">幸福</font><br /> 能和心爱的人一起睡觉，是件幸福的事情；可是，打呼噜怎么办？<br />
								<div>
									<p style="font-size: 13px;padding-top: 5px;float: left;">18分钟前</p>
									<a href="#popover" id="openPopover" class="mui-icon mui-icon-compose" style="float: right;"></a>
								</div>
							</div>
						</li>
					</ul>
					<ul class="mui-table-view">
						<li class="mui-table-view-cell mui-media" style="width: 100%;">
							<img class="mui-media-object mui-pull-left" src="../img/3.jpg">
							<div class="mui-media-body" style="">
								<font color="#2187E7">幸福</font><br /> 能和心爱的人一起睡觉，是件幸福的事情；可是，打呼噜怎么办？<br />
								<div>
									<p style="font-size: 13px;padding-top: 5px;float: left;">18分钟前</p>
									<a href="#popover" id="openPopover" class="mui-icon mui-icon-compose" style="float: right;"></a>
								</div>
							</div>
						</li>
					</ul>
				</div>
				
				
				</div></div>
		<script src="../js/mui.min.js"></script>
		<script type="text/javascript" src="../js/jquery-1.11.0.min.js"></script>
		<script type="text/javascript">
			
			mui.init({
				pullRefresh: {
					container: '#pullrefresh',
					down: {
						style:'circle',
						callback: pulldownRefresh
					},
					up: {
						callback: pullupRefresh
					}
				}
			});
			
			var down=1,up=1;
			
			//下拉
			function pulldownRefresh(){
				setTimeout(function(){
				var html="<ul class=\"mui-table-view\">"+
							"<li class=\"mui-table-view-cell mui-media\" style=\"width: 100%;\">"+
								"<img class=\"mui-media-object mui-pull-left\" src=\"../img/3.jpg\">"+
								"<div class=\"mui-media-body\" style=\"\">"+
									"<font color=\"#2187E7\">幸福"+down+"</font><br /> 能和心爱的人一起睡觉，是件幸福的事情；可是，打呼噜怎么办？<br />"+
									"<div>"+
										"<p style=\"font-size: 13px;padding-top: 5px;float: left;\">18分钟前</p>"+
										"<a href=\"#popover\" id=\"openPopover\" class=\"mui-icon mui-icon-compose\" style=\"float: right;\"></a>"+
									"</div>"+
								"</div></li></ul>";
						$("#dataList").html(html+$("#dataList").html());
					down++;
					mui("#pullrefresh").pullRefresh().endPulldownToRefresh();
					},2000);
			}
			//上拉
			function pullupRefresh(){
				setTimeout(function(){
					var html="<ul class=\"mui-table-view\">"+
							"<li class=\"mui-table-view-cell mui-media\" style=\"width: 100%;\">"+
								"<img class=\"mui-media-object mui-pull-left\" src=\"../img/3.jpg\">"+
								"<div class=\"mui-media-body\" style=\"\">"+
									"<font color=\"#2187E7\">幸福"+up+"</font><br /> 能和心爱的人一起睡觉，是件幸福的事情；可是，打呼噜怎么办？<br />"+
									"<div>"+
										"<p style=\"font-size: 13px;padding-top: 5px;float: left;\">18分钟前</p>"+
										"<a href=\"#popover\" id=\"openPopover\" class=\"mui-icon mui-icon-compose\" style=\"float: right;\"></a>"+
									"</div>"+
								"</div></li></ul>";
						$("#dataList").append(html);
					up++;
					mui("#pullrefresh").pullRefresh().endPullupToRefresh();
				},2000);
				
			}
			
			
		</script>
	</body>

</html>
```

# 打包与部署

