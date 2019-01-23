本人统一将源码包安装到/usr/local/src，软件安装到/usr/local下

##1.下载jdk
去oracle官网(https://www.oracle.com/technetwork/java/javase/downloads/index.html)下载jkd,将安装包上传至服务器/usr/local/src目录下

解压

`# tar zxvf jdk-8u191-linux-x64.tar.gz\?AuthParam\=1540353430_f65dbaa1cedb55bd47708b24615ed931`

移动软件包到/usr/local/jdk

`# mv jdk1.8.0_191/ /usr/local/jdk`

配置jdk环境变量

`# vim /etc/profile`

将以下代码写在文件末尾


export JAVA_HOME=/usr/local/jdk

export CLASSPATH=.:${JAVA_HOME}/jre/lib/rt.jar:${JAVA_HOME}/lib/dt.jar:${JAVA_HOME}/lib/tools.jar

export PATH=$PATH:${JAVA_HOME}/bin


CentOS6上面的是JAVAHOME，CentOS7是{JAVA_HOME}

配置生效：`# source /etc/profile`
有提示版本就标识成功：`# java -version`
`# javac -version`