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

### git的push网络失败问题
下载ghelper配套的clash Window版软件，见当前目录的压缩包Clash-for-Windows-0.20.8-x64-CN
启动Clash软件，设置Clash订阅
![](img/useClashWin.jpg)
- 对github设置代理,
```bash
#使用socks5代理（推荐）
git config --global http.https://github.com.proxy socks5://127.0.0.1:7890
#使用http代理（不推荐）  但是有效
git config --global http.https://github.com.proxy http://127.0.0.1:7890
```
- 对github查看代理
```bash
 git config --global --get http.https://github.com.proxy
```
- 对github取消代理
```bash
 git config --global --unset http.https://github.com.proxy
```
上述端口见
![](img/proxyPort.jpg)
