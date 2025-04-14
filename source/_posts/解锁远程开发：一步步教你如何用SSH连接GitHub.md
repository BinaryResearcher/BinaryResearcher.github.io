---
title: 解锁远程开发：一步步教你如何用SSH连接GitHub
date: 2024-09-13 01:10:44
tags: github
category: Linux
---
#
最近想在远程服务器上进行代码开发，原因是自己本地计算机性能不太够，加上想着折腾。才写这篇教程，希望对大家有帮助，如有错误，请指出我的错误，谢谢。
本文假设已经安装了git，同时是第一次创建ssh。
# 配置git信息
1、设置计算机上的信息，由于该计算机是本人使用，所以选择全局创建：
```bash
git config --global user.name "Your Name"
git config --global user.email "your_email@example.com"
```
根据你github上的用户名和邮箱进行替换即可。
2、生成新的 SSH 密钥
```bash
ssh-keygen -t rsa -C "your_email@example.com"
```
注意替换成自己的邮箱，根据提示，直接点回车，说明会在默认文件id_rsa上生成ssh key。（根据需要是否设置密码，我这里直接回车，不需要设置密码）。
# 在github上设置公匙
1、里面有id_rsa和id_rsa.pub两个文件，这两个就是SSH Key的秘钥对，id_rsa是私钥，不要泄露，id_rsa.pub是公钥，可以公开。
2、现在打开打开id_rsa.pub进行复制到回到github网站，进入Account Settings，左边选择SSH Keys，Add SSH Key,填写你想填的title，粘贴key。
3、验证是否成功，在git bash下输入
```bash
ssh -T git@github.com
```
回车就会看到：You’ve successfully authenticated, but GitHub does not provide shell access 。这就表示已成功连上github。开始你的github吧。