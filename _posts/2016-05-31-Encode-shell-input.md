---
layout: post
title:  "隐藏shell输入的内容"
date:   2016-05-31 13:29:01
categories: linux
tags: linux shell
---

* content
{:toc}

在shell脚本中如需获取手动输入的内容,一般会使用下面的代码:

> read choice

这样就可以将输入内容保存到 choice变量中,同时在命令行窗口中会打印输入的内容.

但如果需手动输入的是密码之类的敏感信息就会有泄漏的危险,只需将上面的代码改为:

> read -s choice

这样在手动输入的时候就不会同时打印输入的内容了.
