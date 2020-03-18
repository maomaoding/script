# script
脚本插件
在登录远程服务器的时候使用命令：
ssh -L 16006:127.0.0.1:6006 account@server.address
（代替一般ssh远程登录命令：ssh account@server.address）
训练完模型之后使用如下命令：
tensorboard --logdir="/path/to/log-directory"
（其中，/path/to/log-directory为自己设定的日志存放路径，因人而异）
最后，在本地访问地址：http://127.0.0.1:16006/
原理
建立ssh隧道，实现远程端口到本地端口的转发 具体来说就是将远程服务器的6006端口（tensorboard默认将数据放在6006端口）转发到本地的16006端口，在本地对16006端口的访问即是对远程6006端口的访问，当然，转发到本地某一端口不是限定的，可自由选择。

# Resources
[Cambridge University Press is making higher education textbooks in HTML format free to access online during th coronavirus outbreak](https://www.cambridge.org/core/what-we-publish/textbooks)