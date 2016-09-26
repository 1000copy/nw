nw
==

有道词典客户端。超级简洁。只有单词输入和查询结果。

使用nodewebkit 制作，一个上午时间搞定。

唯一遗憾的就是，包太大了。

打包方法（目前仅仅支持windows）

1. 按照 Nodewebkit
2. 把git内容拷贝到 Nodewebkit 目录下
3. 执行 r.bat 


## 时隔三年后的今日2016年09月26日

一直想用javascript来做桌面应用，特别是delphi，c++日趋没落的情况下。何况，js的runtime环境的基数巨大，比一般脚本来说具备无可比拟的优势。

但是现有的方案，如node-webkit , Electron 都有一个共同的问题，就是发布包太大，一个helloworld也得50M。

前些天一个前同事推荐了sciter，我发现可以使用html/css以及它的自定义脚本tiscript来编写客户端程序。此人公司内在使用它，写了些小程序，说是效果很好。并且打包很小，压缩下来2M的样子。

我就试试，把我以前写的一个词典客户端改写出来，在OSX上，大概用了2小时的样子。文件在目录2内：

###测试

1. 下载sciter SDK，并且解压(from http://sciter.com/)
2. 执行bin.osx/sciter，使用它打开<HOME>/2/default.htm
3. 在框内输入单词，点击get，看到单词解释

说明代码执行成功。

###打包

1. 编译demo.osx/layered/...xcodeproject
2. 用<HOME>/2/default.htm 替换此工程内res/default.htm
3. chmod +x compile-res.sh && ./compile-res.sh
4. Build & Run

此产品打包完毕