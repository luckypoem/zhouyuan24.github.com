#smpt发送失败php_network_getaddresses


今天邮箱服务器发送失败，查看log日志，
		
		出现SMTP错误: 0 php_network_getaddresses: getaddrinfo failed: Temporary failure in name resolution<br />无法发送数据: AUTH LOGIN<br />发送AUTH LOGIN命令失败. 错误为: <br />无法发送数据:
		
###解决步骤
1. 先`ping` 下smtp服务器是否可以`ping` 的通，我这边是出现错误
		
		ping: unknown host smtpcloud.sohu.com
2. 配置DNS 可以选择IDC给你DNS, 也可以使用google共用的
		
		# cat /etc/resolv.conf
         nameserver 8.8.8.8    #（Google的公共DNS服务）
         nameserver 8.8.4.4    #（Google的公共DNS服务）
3. 尝试继续发送，如果还是无法发送，则修改host文件
		
		vi /etc/hosts 
		某ip  smtpcloud.sohu.com
4. 我这边就可以成功发送邮件了。		         				