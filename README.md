# 关于悟空安全实验室
过去几年中, 随着开源代码组件和开源代码社区的大量增长，开源漏洞的数量也在不断增加。2019年报告的开放源代码漏洞数量增加了近50％，悟空安全实验室致力于帮助企业在开发流程中最大程度避免有漏洞的组件被调用，帮助企业有效提升产品的安全性。

### gokusec cli 用法
```
[root@10-13-106-74 cli]# gokucli  --help
gokucli - An open source component security detection tool.

Usage:
  gokucli [flags]
  gokucli [command]

Available Commands:
  auth        login, logout, and refresh your apiToken.
  help        Help about any command
  scan        

Flags:
  -h, --help      help for gokucli
  -v, --version   version of gokucli

Use "gokucli [command] --help" for more information about a command.
```
1）首先登陆 http://gokusec.com/ ,进入控制台点击`查看TOKEN`获取自己的token信息:0e039c1f089718df49a062b82ab8e4ce987kw829

2）使用token登陆gokusec cli

`gokucli auth login`

3）检测指定目录的代码第三方组件安全风险，指定的代码目录一定要包含pom.xml文件

`gokucli scan /home/work/code/crm/`

4）等待扫描结束后登陆 http://gokusec.com/ 控制台查看结果
