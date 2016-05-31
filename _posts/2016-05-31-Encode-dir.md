---
layout: post
title:  "linux下使用tar加密解密文件夹"
date:   2016-05-31 13:28:46
categories: linux
tags: linux tar openssl
---

* content
{:toc}

加密文件夹:

> tar -zcvf - dir_path \| openssl des3 -salt -k passwd \| dd of=dir_name.des3

注意修改 dir_path为需加密文件夹的路径,passwd为加密的密码, dir_name为加密后des3文件的名称

解密文件夹:

> dd if=unlock_file_path \| openssl des3 -d -k passwd \| tar zxf -

注意修改 unlock_file_path为需解密的文件名称,passwd为加密的密码
