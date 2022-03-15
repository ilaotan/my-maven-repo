# my-maven-repo
使用Github作为第三方依赖包的托管仓库

命令  
```
mvn clean source:jar deploy -DaltDeploymentRepository=my-repo::default::file:E:\svnRepository\githubMy\my-maven-repo\repository\

```
如果是jar包,命令则有些许不同
```
mvn install:install-file -DgroupId=com.oracle -DartifactId=ojdbc14 -Dversion=10.2.0.2.0 -Dfile=E:\ojdbc14-10.2.0.2.0.jar -Dpackaging=jar -DgeneratePom=true -DlocalRepositoryPath=E:\01_Work\01_DevSpace\worksapce_github\simbest-maven-repo\repository -DcreateChecksum=true 

```

其他项目添加本仓库的引用  
```
<repository>
    <id>my-maven-repo1</id>
    <url>https://raw.github.com/ilaotan/my-maven-repo/master/repository/</url>
    <snapshots>
        <enabled>true</enabled>
        <updatePolicy>always</updatePolicy>
    </snapshots>
</repository>
```

2022年3月15日 更新
可以使用 https://jitpack.io 来作为版本坐标.
example: https://github.com/nacos-group/nacos-spring-boot-project/issues/185
```
<repositories>
	  <repository>
		    <id>jitpack.io</id>
		    <url>https://jitpack.io</url>
	  </repository>
</repositories>
<dependency>
	  <artifactId>nacos-config-spring-boot-starter</artifactId>
	  <groupId>com.github.nacos-group.nacos-spring-boot-project</groupId>
	  <version>93641fbbc57e583f93b70d71168fef9035a026e2</version>
</dependency>
```
