# GIT默认忽略文件名大小写变化怎么解决
- git在提交代码时，会忽略文件名称大小写，导致本地代码与远程代码不一致，此时可利用终端指令git config --get core.ignorecase来检查下
- 可以通过设置来关闭忽略git config core.ignorecase false