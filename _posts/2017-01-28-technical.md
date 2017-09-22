---
layout: post
title: 技术日志
published: true
---
为了监督个人的学习进步，本文档的建立用以记录科技学习中（包括建立网站、学习数据科学、计算机科学）的技术问题的解决：

**01/16/17 成功利用Jekyll搭建网站**

- 利用fork在github网站上实现了网站的运行
- 在local server上安装ruby、jekyll、以及用以打开代码的notepad
- 成功在本地host上调试生成网页，并利用电脑版github成功同步

**01/18/17 - 01/20/17 安装RapidMiner并完成clustering实现**

- 了解RapidMiner的基本用法
- 运用如下operator：select attributes, EM, clustering
- 完成clustering作业

**01/22/17 解决jekyll上表格无法生成border以及无法更改width**

- 在scss文档中增加新函数，并在生成表格的代码下使用该函数(不能空格)
- 参考文档
  + http://www.w3schools.com/css/css_table.asp
  + http://stackoverflow.com/questions/28806135/jekyll-kramdown-how-to-display-table-border
- 小经验：以后现在localhost上运行后再同步，本地服务器没有延后。

**01/24/17 参与周一meeting session了解如何利用Clustering挖掘数据结构**

- 在处理数据时，第一步先用Excel大致查一下数据分布（或计算），无大问题的前提下，先进行standardized（标准化），使得数据处在相同的scale上。
- 一般clustering是做多个变量的结构分析，若做单一变量的clustering，实际上就是按照平均值区分。
- 在多个变量的前提下，可以先包含所有可能变量分析结构（别忘记联系实际），可以参考centroid的差异来判断clustering是否明显。
- 在进行聚类分析后，可以根据不同组别分别分析，比如在回归分析中，可以将这个组别dummy coding，纳入分析。 
- 关键就是，聚类分析没有一个严格意义上的performance指标，一切从实际需求出发，由问题决定。 

**01/28/17 利用disqus给博客增加评论功能**

**02/02/17 利用R解决提出单行重复值的问题，生成了Peer Affiliation Coding的最终版**

- 利用unique()函数将data.frame变为matrix，然后重新生成新的matrix
- 另外，学习到了apply函数的用法，即不需要管数据类型（either matrix or data.frame），将函数用于数据结构中的单个元素上。

**02/20/17 利用JAVA成功运行A'程序** 

- 在电脑上安装JDK 8,添加环境变量。 [http://www.runoob.com/java/java-environment-setup.html](http://www.runoob.com/java/java-environment-setup.html)
- 利用CMD运行JAVA代码，生成Class，然后依照A'程序指示运行得到A’。
- 意识到JAVA跨平台语言的含义，即了解到常用eclipse作为JAVA的集成环境（integrated development envrionment)
- compile java file using "javac name.java", run using "java name"

**03/03/2017 利用R解决了peer group identification的问题，帮助拥有多重组别的学生迅速定位主要组别**

- 利用subset()和duplicate()实现matrix之间的数据选择
- 比较两个vector之间是否存在相同的值，利用 %in% operator，返回逻辑值

**09/21/2017 在辗转求索于一个最优的信息管理系统和文献引文管理系统中，遇见了Zotero**

- Zotero是一款开源的帮助收集、整理和分享信息的开源独立软件（standalone desktop application)，因其开源特性，故也有很多插件与之相配套。
- 在与Mendley、Refworks以及Noteexpress比较之后，选择Zotero原因如下：
	- Mendely作为自带pdf阅读器功能，却变得无比繁重，尤其是在加入同步这一功能后，打开速度之慢让人不免焦躁。
   - Refworks没有desktop application版本，且有时候归类时容易陷入繁琐的境地，且回国后因为网速和墙的限制仍然不是很便捷。
   - Zotero最强大的在于web translator功能，能够自行识别网站的信息并进行相应的归类，大大扩展了信息管理的范围，而不只局限于文献；且与各种插件搭配使用，最大限度地方便了操作。
