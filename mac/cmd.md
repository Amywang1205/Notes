> 删除当前目录下的.DS_Store文件 

  `find . -name '*.DS_Store' -type f -delete`
  
> 80端口映射

  跳转至/etc目录下       ` cd /etc`

  打开pf.conf文件，在    `rdr-anchor "com.apple/*"`下方，添加或者修改 `rdr on lo0 inet proto tcp from any to 127.0.0.1 port 80 -> 127.0.0.1 port 8080`
  之后依次执行`sudo pfctl -d    sudo pfctl -f /etc/pf.conf  sudo pfctl -e`

> 允许显示安装任何来源的软件

 `sudo spctl --master-disable`

