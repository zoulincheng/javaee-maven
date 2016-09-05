http://www.cnblogs.com/xdp-gacl/p/4068967.html

怎么添加到本地仓库呢？
步骤：
1.cmd命令进入该jar包所在路径
2.执行命令
mvn install:install-file -Dfile=lucene-queryparser-4.6.1.jar -DgroupId=org.apache.lucene -DartifactId=lucene-queryparser -Dversion=4.6.1 -Dpackaging=jar
（不同的jar包相对应替换对应部分）

mvn install:install-file -Dfile=groovy-1.8.3.jar -DgroupId=org.codehaus.groovy -DartifactId=groovy -Dversion=1.8.3 -Dpackaging=jar