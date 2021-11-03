# chia-toolbox

## hpool自动提现助手

1. 仅支持Linux系统运行
2. 需使用Python3.8以上版本
3. 需要手动完善请求头中的cookie
4. Google Authenticator自动获取依赖`oathtool`工具以及绑定`Google Authenticator`时的备份key



获取提现工具

```
git clone https://github.com/ripmars/chia-toolbox
```

获取cookie请自行查询获取.

修改脚本补充cookie内容

安装`oathtool`

```shell
sudo apt install oathtool gnupg2 
```

> 参考链接: [Use oathtool Linux command line for 2 step verification (2FA)](https://www.cyberciti.biz/faq/use-oathtool-linux-command-line-for-2-step-verification-2fa/)

安装完成之后创建脚本`totp.sh`,文件内容为:

```shell
oathtool -b --totp '绑定Google Authenticator时的备份key'
```



telegram bot申请以及获取id请参见：[教程|Telegram Bot 搭建](https://zhuanlan.zhihu.com/p/59228574)



创建定时任务每天执行

建议下午三点以后，五点以前
