----------------
Godw

<a href="https://godoc.org/github.com/nulijiabei/godw"><img src="https://godoc.org/github.com/nulijiabei/godw?status.svg" alt="GoDoc"></a>

网络文件管理
	
	通过一个简单的页面，来将重要的文件存储到云端 ...
	通过一个简单的页面，来方便讲云端文件下载本地 ...

[PATH]

    [godw]     主程序
    [files]    存储目录
    [template] 模版文件

注意：主程序需要在[PATH]目录下执行,因为程序内部使用的相对目录,当然,你也可以修改为绝对目录

因为偷懒，所以并没有讲目录文件信息记录到数据库或者记录文件内，而是每次遍历，非常浪费资源

如果程序在环境并发很高的话，建议修改记录到数据库等

[UPDATE]

	增加权限管理,[session]
	
	通过登陆时设置的权限参数[www.xxx.com?admin]来设置全局权限
	-- 这里的admin是godw.conf中所指定的
	
	无权限者,只能访问列表目录，查看，下载，无法进行添加，删除操作
	
	普通该用户，可以添加，查看，下载，无法删除操作
	
	管理员，添加，查看，下载，删除，均可

[ Linux Bash 上传 ]

	curl -F "file=@a.jpg;filename=a.jpg"  http:/xxx.xxx.com:8080/upload.go
	curl -F "file=@a.jpg;filename=a.jpg"  http:/xxx.xxx.com:8080/upload.go?overlay=true

----------------

![image](https://raw.githubusercontent.com/nulijiabei/godw/master/screenshot.png)


