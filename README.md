### github不再支持密码认证,而是使用token认证

#### 1 生成个人token

#### 2 克隆项目到本地

```bash
git clone  https://github.com/teaCupa/configRepo.git
```

#### 3 git push 推送更改到远程仓库

首先，在本地git中进行如下操作：

```shell
# 移除原来的远程链接
git remote remove origin
# 查看git的远程链接
git remote -v
# 重新新增git远程链接
git remote add origin https://<your token>@github.com/<your account>/<your repository>.git
                   <your account> 即teaCupa   <your token>见gitee的git练习项目
# push到远程
git push --set-upstream origin main
```

