#**`Linux环境下安装JDK1.8`**


###1.通常情况下安装在/usr/local目录下
###2.查看虚拟机现有jdk版本：rpm -qa|grep jdk，如果不合适，将其卸载
###3.下载后拷贝至linux后解压：
    tar  -zxvf  jdk-8u131-linux-x64.tar.gz   z代表gzip的压缩包；x代表解压；v代表显示过程信息；f代表后面接的是文件 .
###4.修改环境变量
    export JAVA_HOME=/usr/local/jdk1.8.0_251  //此路径为jdk解压后目录,版本号需与实际保持一致
    export JRE_HOME=${JAVA_HOME}/jre
    export CLASSPATH=.:${JAVA_HOME}/lib:${JRE_HOME}/lib:$CLASSPATH
    export JAVA_PATH=${JAVA_HOME}/bin:${JRE_HOME}/bin
    export PATH=$PATH:${JAVA_PATH}
###5.重启配置信息
    source /etc/profile
###6.检测 
    java -version  查看现有java版本
    
    