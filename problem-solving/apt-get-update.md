# sudo apt-get update failed or stuck

etc/apt/sources.list is the problems. Ubuntu更新源问题. https://wiki.ubuntu.com.cn/%E6%BA%90%E5%88%97%E8%A1%A8


最终解决方案：

```
1. open https://mirror.tuna.tsinghua.edu.cn/help/ubuntu/
2. copy it into /etc/apt/source.list
3. sudo apt-get update
```
## ubuntu update source

[official website](http://manpages.ubuntu.com/manpages/zesty/en/man5/sources.list.5.html)

The source list /etc/apt/sources.list and the files contained in `/etc/apt/sources.list.d/`
 are designed to support any number of active sources and a variety of source media. 

- sources 到底是什么鬼？

源就是软件的来源。  
当你运行apt-get install xxx的时候，apt-get这个程序会从所设置的源下载需要的.deb的包，apt会自动处理软件之间的依赖关系。  
在apt出现之前，你必须自己判断如果要安装A软件，必须先安装C软件这样的问题。
因为linux是集市开发模式，是像积木一样搭起来的，好处是你可以只用你需要的，缺点是你必须清楚你需要什么。
刚安装好的时候，/etc/apt/sources.list中，只有安装盘这一个源，而这个盘上之后运行系统所必须的安装包。你要用其他的软件，就必须设置新的源。  
ubuntu这个发型版的源由Canonical公司来维护，他们负责从linux的汪洋大海中选取一些稳定的、实用的程序加入源中，即http://us.archive.ubuntu.org这个源。其他的源都是通过rsnyc与这个源同步的。  
Canonical公司是非营利的，主要由Shuttle Worth这个猪头出资支持。
