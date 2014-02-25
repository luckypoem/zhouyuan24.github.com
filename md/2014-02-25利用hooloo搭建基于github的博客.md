#利用Hooloo搭建基于github的博客
###小引
 之前尝试使用`Octopress`来搭建，因为mac的ruby问题，没有安装成功，今天在一次巧合下，看到 [`Hooloo`](https://github.com/sneezry/Hooloo)这个非常轻量的博客系统，相对`Octopress`来说更加简单。
 
 
 
###目录
 1. 设置github账号
 2. 安装Hooloo
 3. 将博客部署到GitHub上
 4. 开始写博客
 5. 域名解析
 6. 小结
 
 
###设置github账号
 基于github的博客当然需要先注册github账号，Github的账号注册地址是：<https://github.com/signup/free> 。申请好github账号后，建一个名为 username.github.com 的代码仓库。这里注意username必须是和你的账号名一致。 我的是username为zhouyuan24,所以新建的代码仓库是[zhouyuan24.github.com](https://github.com/zhouyuan24/zhouyuan24.github.com)
 
###安装Hooloo
* 在安装Hooloo之前，请确保你的电脑上已经安装有git了，在终端输入git --version，应该可以看到电脑中的git版本
* 下载[Hooloo](https://github.com/sneezry/Hooloo/archive/master.zip)
* 将之前创建的代码仓库拉到本地，拷贝Hooloo到代码仓库，修改 `javascripts/config.js`,以我的为例   
		
		var disqus_shortname = 'zhouyuan24';
	    var hostbase = 'http://zhouyuan24.github.com';
		var githubname = 'zhouyuan24';
		var repos = 'zhouyuan24.github.com';
		var sitetitle = '周渊的博客';
		var rss = '';	
`disqus_shortname` 去<http://disqus.com>申请，用于博客评论的

* 最后提交代码到github commit and push到github上，
* 我们就可以在浏览器中使用页面地址http://username.github.com来访问我们的博客


###开始写博客
md目录文章保存地址，我用的markdown编辑器是[Mou](http://mouapp.com/),文件保存名必须是时间+文章名称，类似2014-02-25helloword.md 

###域名解析
如果你象我一样有自己的域名，可以将域名指向这个博客，具体步骤是：

* 在域名管理中，建立一个CNAME指向，将你的域名指向 yourname.github.com
* 修改CNAME的文件，然后将自己的域名输入进去。我的是blog.zhouyuan11.cn
* 将内容push到github后，第一次生效大概等1小时，之后你就可以用自己的域名访问了。

###小结
`index.html` 可以修改首页的样式
 大家在搭建过程中有问题可以回复我。
 

