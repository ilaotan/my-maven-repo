# my-maven-repo
使用Github作为第三方依赖包的托管仓库，实现公网的Maven私服Nexus

命令  
```
mvn clean source:jar deploy -DaltDeploymentRepository=my-repo::default::file:E:\svnRepository\githubMy\my-maven-repo\repository\

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