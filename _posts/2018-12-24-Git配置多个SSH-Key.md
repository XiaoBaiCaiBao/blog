---
title: Git配置多个SSH-Key
layout: post
---
# C:\Users\Cathrine\\.ssh

## 删除之前的密钥
> rm ~/.ssh/id_rsa.pub  
rm ~/.ssh/id_rsa

## 生成新的密钥
> ssh-keygen -t rsa -C '626183362@qq.com' -f ~/.ssh/gitee_id_rsa
ssh-keygen -t rsa -C '626183362@qq.com' -f ~/.ssh/github_id_rsa

参考文章
[1] https://gitee.com/help/articles/4229#article-header0 "Git配置多个SSH-Key"

## 取消原全局git账号设置（没用，依然是全局设置的）
> git config --global --unset user.name  
git config --global --unset user.email  
git config -l # 查看当前目录的git config

## 分别去不同的项目目录中，设置这个目录中项目对应的账号（没用，依然是全局设置的）
> git config user.name "CathrineBao"  
git config user.email "626183362@qq.com"  

> git config user.name "babyBao"  
git config user.email "626183362@qq.com"