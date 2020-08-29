# 配置

?> 为了满足项目需求，对bootstrap5的默认样式进行深度定制。

## 配置目录结构

📂 **css**  
|— 📂 bootstrap5-scss   
| &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; |__ bootstrap5原版.scss配置文件  
|— 📂 my_scss  
| &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; |__ 自定义.scc文件  
| _bootstrap5.scss  ———— 指定bootstrap5可生成的.scss包内容  
| all.scss   ———— 指自定义.scc包内容 + _bootstrap5.scss包内容  
| all.css  
| all.min.css 

## vscode编译scss插件配置

为了方便编译scss文件，首先需要在vscode中安装.scss文件编译插件
- 插件名称：`Live Sass Compiler`
- [插件地址](https://marketplace.visualstudio.com/items?itemName=ritwickdey.live-sass)
- [github文档](https://github.com/ritwickdey/vscode-live-sass-compiler/blob/master/docs/settings.md)

插件配置：打开vscode的设置`settings.json`插入如下配置代码

```json
//sass编译插件设置：https://github.com/ritwickdey/vscode-live-sass-compiler/blob/master/docs/settings.md
"liveSassCompile.settings.formats":[
	// This is Default.
	{
		"format": "expanded", //指定编译css的样式类型，有这四种 expanded（默认）, compact, compressed or nested
		"extensionName": ".css",  //指定编译完的文件后缀名，.css为普通代码，.min.css为压缩代码
		"savePath": null
	},
	// You can add more
	{
		"format": "compressed",
		"extensionName": ".min.css",
		"savePath": null
	}
],
"liveSassCompile.settings.generateMap":false,//关闭.map文件生成
```
配置好之后在vscode右下角会出现 `@Watch Sass`按钮，点击即可进行.scss快速编译。

