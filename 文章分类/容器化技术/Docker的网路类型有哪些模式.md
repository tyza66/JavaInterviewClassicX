# Docker的网络类型有哪些模式
- bridge模式：docker默认的网络模式，可以设置ip，但是要与docker host主机的虚拟网络在同一个网段
- none模式：不会给容器进行任何的网络配置
- host模式：容器与docker host主机共享网络，容器的端口与docker host主机的端口一致
- container模式：与已存在的容器共有同一个ip地址
- network模式：可以自定义网络，容器之间可以通过容器名进行通信（docker network create）