---
layout: post/test
title: "git生成SSH并提交"
date: 2019-08-19 
tags: Git  
---

### 1. 生成秘钥 
$ ssh-keygen -t rsa -C "fengming19981221@163.com" 
按3个回车，密码为空这里一般不使用密钥。 
最后得到了两个文件：id_rsa和id_rsa. pub 在 ～下的.ssh文件夹中 
 
### 2. 查看秘钥
cat ~/.ssh/id_rsa.pub   

### 3. 添加私密钥到ssh：ssh-add ~/.ssh/id_rsa   
需要之前输入密码（如果有）。
 
### 4. 在github上添加ssh密钥，这要添加的是“id_rsa.pub”里面的公钥。   
在第二步中，将结果复制下来
设置--》部署秘钥--》添加部署秘钥

### 5. 克隆SSH协议的存储库   
git clone git@github.com:victorfengming/victorfengming.github.io.git

### 6. 推他就完了   
git add --all   
git commit -m”SSH有瑕疵“  
git push -u origin master  


***
### 版权说明

***
如需转载请注明出处：[凤明的博客](https://victorfengming.github.io/#blog) » https://victorfengming. github. io/#blog

本文链接：[git生成SSH并提交](https://victorfengming.github.io/2019/08/github-generate-ssh/) » https://victorfengming. github. io/2019/08/github-generate-ssh/)

***
大家可以关注小编的CSDN：[秋叶夏风的博客](https://blog.csdn.net/qq_40223983) » https://blog. csdn. net/qq_40223983

***