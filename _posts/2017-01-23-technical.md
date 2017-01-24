---
layout: post
title: 技术日志
---
为了监督个人的学习进步，本文档的建立用以记录跟此网站建立相关的技术问题的解决：

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
