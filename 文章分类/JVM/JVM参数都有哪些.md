# JVM参数都有哪些
- 标注指令：-开头，如-Xms，-Xmx 是所有的HotSpot都支持的参数，可以用java -help打印出来
- 非标注指令：-X开头，这些指令通常是特定的HotSpot版本对应的，可以用java -X打印出来
- 不稳定参数：-XX开头，这些参数在不同版本的HotSpot中可能会有不同的表现，甚至不同的默认值，可能会在下个版本中被取消，可以用java -XX:+PrintFlagsFinal -version打印出来，详细的资料非常稀少
- 在java1.8中有几个不稳定参数：
java -XX:+PrintCommandLineFlags ： 查看当前命令的不稳定指令。
java -XX:+PrintFlagsInitial ： 查看所有不稳定指令的默认值。
java -XX:+PrintFlagsFinal： 查看所有不稳定指令最终⽣效的实际值