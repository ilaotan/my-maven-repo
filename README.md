# my-maven-repo
使用Github作为第三方依赖包的托管仓库，实现公网的Maven私服Nexus

命令  
```
clean source:jar install -DcreateChecksum=true
```

从本地库里拷贝对应文件夹复制到当前的repository里,注意剔除 _remote.repositories(没试过不剔除是什么效果,应该影响不大)

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