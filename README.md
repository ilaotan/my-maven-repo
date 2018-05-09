# my-maven-repo
使用Github作为第三方依赖包的托管仓库，实现公网的Maven私服Nexus

命令  
`
clean source:jar install -DcreateChecksum=true
`

从本地库里拷贝对应文件夹,注意剔除 _remote.repositories(没试过不剔除是什么效果,应该影响不大)