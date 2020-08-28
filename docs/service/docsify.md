# docsify配置

index.html配置
```html
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>ue-wiki</title>
	<meta http-equiv="X-UA-Compatible" content="IE=edge,chrome=1" />
	<meta name="description" content="Description">
	<meta name="viewport" content="width=device-width, user-scalable=no, initial-scale=1.0, maximum-scale=1.0, minimum-scale=1.0">
	<link rel="stylesheet" href="//cdn.jsdelivr.net/npm/docsify/lib/themes/vue.css">
</head>
<body>
<div id="app"></div>
<script>
window.$docsify = {
	logo: 'https://docsify.js.org/_media/icon.svg',   // 配置网站logo '/_media/icon.svg'
	name: 'uewiki',       // 文档标题，会显示在侧边栏顶部
	nameLink: 'http://localhost/uewiki/docs/#/',  // 文档标题链接，可配置路由 详见：https://docsify.js.org/#/zh-cn/configuration?id=namelink
	// themeColor: '#3F51B5',    // 配置主题颜色
	repo: '',
	// homepage: 'home.md', // 手动指定首页，默认 README.md,也可以直接填写互联网的.md的url地址
	coverpage: true,    // 开启封面
	onlyCover: true,   // 只在首页时加载封面
	loadNavbar: true,   // 开启导航条
	loadSidebar: true,  // 开启侧边导航
	// autoHeader: true,   // 同时设置 loadSidebar 和 autoHeader 后，可以根据 _sidebar.md 的内容自动为每个页面增加标题
	// hideSidebar: true,   // 完全关闭侧边栏
	// onlyCover: true,   // 封面作为独立首页
	// coverpage: ['/', '/zh-cn/'],   // 多个封面：每个目录独立封面
	// maxLevel: 3,   // 渲染层级
	// auto2top: true,   // 切换页面后是否自动跳转到页面顶部
	// basePath: '/path/',   // 整站文档根路径，可以是二级路径或者是其他域名的路径 例如：'https://docsify.js.org/'
	// relativePath: true,   // 启用网址结构相对路径（默认：false）详见：https://docsify.js.org/#/zh-cn/configuration?id=relativepath
	mergeNavbar: true,    // 移动端设备下 合并顶部导航栏到侧边栏
	// externalLinkTarget: '_self', // default: '_blank' 外部链接的打开方式
	// cornerExternalLinkTarget: '_self', // default: '_blank' 右上角链接的打开方式
	// notFoundPage: true,   // 开启404功能，需手动添加文件_404.md
	topMargin: 90, // default: 0 让你的内容页在滚动到指定的锚点时，距离页面顶部有一定空间。当你使用 固定页头 布局时这个选项很有用，可以让你的锚点对齐标题栏

	plugins: [
		// 页尾插件
		function(hook) {
			var footer = [
				'<hr/>',
				'<footer>',
				'<span><a href="https://lee.cm">Jim</a> &copy;2020.</span>',
				'<span>Power by <a href="https://github.com/docsifyjs/docsify" target="_blank">docsify</a>.</span>',
				'</footer>'
			].join('');

			hook.afterEach(function(html) {
			return html + footer;
			});
		},
		// 编辑按钮插件
		function(hook, vm) {
			hook.beforeEach(function(html) {
				var url =
				'https://github.com/popdo/uewiki/tree/master/docs/' +
				vm.route.file;
				var editHtml = '[📝 编辑文档](' + url + ')\n';

				return (
				editHtml +
				html +
				'\n----\n' +
				'Last modified {docsify-updated} ' +
				editHtml
				);
			});
		}
	]
}
</script>
<script src="//cdn.jsdelivr.net/npm/docsify/lib/docsify.min.js"></script>
<script src="//cdn.jsdelivr.net/npm/docsify/lib/plugins/emoji.min.js"></script>

<!-- 加载图片缩放插件：忽略某张图片写法：![](image.png ":no-zoom") -->
<script src="//cdn.jsdelivr.net/npm/docsify/lib/plugins/zoom-image.min.js"></script>

<!-- 代码复制功能 -->
<script src="//cdn.jsdelivr.net/npm/docsify-copy-code"></script>

<!-- 添加prism代码高亮支持的语法：默认已经支持： -->
<script src="//cdn.jsdelivr.net/npm/prismjs@1/components/prism-bash.min.js"></script>
<script src="//cdn.jsdelivr.net/npm/prismjs@1/components/prism-php.min.js"></script>

</body>
</html>

```