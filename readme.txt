http://www.cnblogs.com/xdp-gacl/p/4068967.html

怎么添加到本地仓库呢？
步骤：
1.cmd命令进入该jar包所在路径
2.执行命令
mvn install:install-file -Dfile=lucene-queryparser-4.6.1.jar -DgroupId=org.apache.lucene -DartifactId=lucene-queryparser -Dversion=4.6.1 -Dpackaging=jar
（不同的jar包相对应替换对应部分）

mvn install:install-file -Dfile=groovy-1.8.3.jar -DgroupId=org.codehaus.groovy -DartifactId=groovy -Dversion=1.8.3 -Dpackaging=jar


//aliyun  maven resp
http://maven.aliyun.com/nexus/?spm=0.0.0.0.inDNBj#welcome


1.1、创建Jave Project
1、使用mvn archetype:generate命令，如下所示：
mvn archetype:generate -DgroupId=com.mycompany.app -DartifactId=myapp -DarchetypeArtifactId=mavenarchetype-quickstart -DinteractiveMode=false

2、使用mvn archetype:create命令，如下所示：
mvn archetype:create -DgroupId=com.mycompany.app -DartifactId=myapp -DarchetypeArtifactId=mavenarchetype-quickstart -DinteractiveMode=false


3、archetype:create命令已经过期，需要使用 archetype:generate 来进行代替

因为我当前使用的是maven3.3的版本，其实从控制台上的错误信息也可看出，报错的是2.4的信息，所以也可猜测出是版本引起来的。
经查文档可看出需要使用generate代替create，即将

mvn archetype:generate -DgroupId=com.chuanliu.c11 -DartifactId=c11searcher

代替之前的

mvn archetype:create -DgroupId=com.chuanliu.c11 -DartifactId=c11searcher

 

4、maven-archetype-plugin 2.4版本的插件有问题，换其它版本进行创建

于是采用以下指令进行尝试，发现可以生成：

mvn org.apache.maven.plugins:maven-archetype-plugin:2.2:create  -DgroupId=com.chuanliu.c11 -DartifactId=c11searcher

 

以上几种方案可能在不同的环境下会有不同可行性，在我本机测试方案3和方案4是可行的。如有朋友有其它解决方案，可以跟我留言。
关于create命令就讲到这里。maven在3.0.5及以上就建议采用genrate命令了，建议大家尽量采用genrate代替create命令。