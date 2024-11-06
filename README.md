# git-playground





```
You don't have any public SSH keys in your GitHub account. You can add a new public key, or try cloning this repository via HTTPS.
```

* 复制git ssh的时候有这个提醒，但是是可以通过ssh git clone的。是否说明git clone不需要公钥私钥？
* 当我把Jasper使用中的公钥上传给Timax的GitHub时，会出现报错！也就是说一个公钥只能被使用一次。







```shell
# 之前
git@github.com:username/git-playground.git
# 修改
git@git-playground:username/git-playground.git


(base) jmjin@JmJindeMacBook-Pro git-playground % git remote -v
origin  git@github.com:TimaxThu/git-playground.git (fetch)
origin  git@github.com:TimaxThu/git-playground.git (push)



```







```git
(base) jmjin@JmJindeMacBook-Pro .ssh % cat config 
Host git-playground
    HostName github.com
    User git
    IdentityFile /Users/jmjin/Desktop/git-playground/.ssh
(base) jmjin@JmJindeMacBook-Pro git-playground % git remote set-url origin git@git-playground:TimaxThu/git-playground.git
(base) jmjin@JmJindeMacBook-Pro git-playground % ssh -T git@git-playground
Hi JasperJin01! You've successfully authenticated, but GitHub does not provide shell access.

```









