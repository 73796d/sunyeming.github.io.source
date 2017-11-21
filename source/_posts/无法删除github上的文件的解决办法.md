---
title: 无法删除github上的文件的解决办法
date: 2017-11-21 13:10:59
tags: github
---

1.  如果此文件夹已被加入git追踪，那么删除方法很简单，只需要将此文件夹删掉，然后提交一下就可以了
2.  如果次文件夹曾经被加入过git追踪，现在被加入.gitignore里了，但是github上还有此文件夹。
	
	解决办法如下：
	
		git rm -r --cached 文件夹路径
		git commit -m '删除忽略的目录 "文件夹名字"'
		git push origin master	
			