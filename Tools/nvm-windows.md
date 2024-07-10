##  nvm-windows & 'nvm' 不是内部或外部命令

开发项目时，会碰到需要切换 node 版本的情况。
MacOS 可以使用 [nvm](https://github.com/nvm-sh/nvm) ，
Windows 则可以使用 [nvm-windows](https://github.com/coreybutler/nvm-windows)

nvmw 的文档非常详细！这里要记录的是安装后，cmd 出现 `'nvm' 不是内部或外部命令，也不是可运行的程序`，
但是 PowerShell 可以正常使用...而 webstorm terminal 默认使用 cmd ...

搜索折腾好一会，尝试了重装 nvmw、核对环境变量，都没解决。于是直接把 webstorm terminal 改成 PowerShell

1. File >>> Settings >>> Tools >> Terminal
2. 设置 Application Settings >>> shell path 为 `C:\Windows\System32\WindowsPowerShell\v1.0\powershell.exe`

ps：也可以改成 git bash

ps：cmd 中复制长字符串，粘贴结果会出现多余空格
