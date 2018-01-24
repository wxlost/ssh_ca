# ssh_ca
快速改为ca登录并且修改默认ssh端口

# 本脚本默认是放在网站下获取并且运行.  git仅为开源作用.

首先在你网站里放置一个文本.文本内容为密钥的公钥,文件名随便你写.
key(脚本文件)也放置网站目录下,并且修改86行里面的网站为你自己的.变量参数请勿动
然后在要安装的机器上运行 (参数-p 表示关闭密码登录)
```
rm -rf ${HOME}/.ssh/authorized_keys;curl -s -o cc-ikey -L 你的网站/key && sh cc-ikey 你的ca文件名 -p
```


# 例如:网站域名 test.com 里面有ca文本并且名字为 AABBAADD 然后放置key,并且修改里面的网站,然后运行脚本为
```
curl -s -o cc-ikey -L test.com/key && sh cc-ikey AABBAADD -p
```