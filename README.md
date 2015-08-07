# ThinkAdmin
###基于ThinkPHP的后台管理面板

1、初始功能模块如下：<br>
（1）菜单配置，对于后台显示的菜单都通过手动进行配置，后续版本可能会进行优化。<br>
（2）权限控制，可以根据配置的菜单进行权限控制。<br>
（3）缓存更新，包含前后端模板更新，数据更新和全局更新（最好有针对性的更新缓存，否则在高并发情况下清空全局缓存会导致突然间的服务器负载过大）。<br>
（4）广告管理，简单分为文本广告和图片广告。<br>
（5）系统配置，可以配置项目全局变量。<br>
（6）系统用户管理，包括系统用户组。<br>
<br>
2、一些常用面板组件说明（具体参照代码）：<br>
（1）分页条（根据Bootstrap样式重写的Page类）。<br>
（2）模态对话框/提示框（可以在点击按钮中配置脚本调用）。<br>
（3）模态内容框。<br>
（4）文件上传（swfUpload组件）。<br>
（5）异步查询/分页。<br>
（6）其他：例如时间控件，日期控件等等。<br>
<br>
说明：因为很多功能组件面板采用的是最新的html5标签和CSS3样式特性，所以需要在最新浏览器中才能看到最佳效果，否则面板会变形或出现脚本错误等问题。


###搭建流程

<code>$ git clone https://github.com/meegle/ThinkAdmin.git
</code>

<code>$ cp ./init_data/App/Common/Conf/config.php ./App/Common/Conf/config.php # 根据自己的情况修改Cookie配置项和数据库连接参数
</code>

<code># 创建初始表结构（在数据库中运行./init_data/sql/*.sql）
</code>

<code># 访问 http://localhost/ThinkAdmin/admin - 管理员账号admin, 初始密码123456
</code>