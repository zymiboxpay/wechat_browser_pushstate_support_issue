# wechat_browser_pushstate_support_issue

微信安卓端浏览器 pushState 支持问题复现代码及其他

这是重现问题的代码，其中 wx.config 里面的各项配置要自己填写，重现问题的步骤如下：

- 填写好 js 回调地址，假设是 http://yoursite.com
- 在根目录启动后台服务器
- 在安卓微信端访问 http://yoursite.com/index.html
- 可以看到 jssdk 配置成功的提示弹出框
- 可以点击按钮上传图片
- 点击链接 Go to other page ，页面会通过 pjax 加载新的页面 http://yoursite.com/other.html
- 这时点击第二个按钮可以看到 permission denied 的提示弹出框

这个问题在 iPhone 上不会出现

重现这个问题的 手机是 三星 Note4 ，Android 版本是 5.1.1 ，微信版本是 6.3.25
