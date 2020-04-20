# 会内 PCR 资料整理
行会/公会名：CLRS真吉尔难（国服）  
欢迎加盟我们的咸鱼行会和本仓库建设！  

目录：  
1. [仓库](#仓库)
   - [使用规则](#使用规则)
   - [提交规则](#提交规则)
   - [合并规则](#合并规则)
   - [公开规则](#公开规则)
2. 内容目录
3. reserve

## 仓库
该词条主要包含本仓库的开发和使用方法。  
- [“使用规则”](#使用规则)条目主要给出了 git 的基本用法、该仓库的克隆问题以及 GitHub 协作功能的使用。  
- [“提交规则”](#提交规则)条目给出了分支的使用和 commit 的提交方法。  
- [“合并规则”](#合并规则)条目给出了各分支 merge 到 master 分支的方法。  
- [“公开规则”](#公开规则)条目给出了基于 MIT 开源协议的一些道德上的约束和使用 pull request 提交的问题。  

请按照流程看一遍，目录供之后方便查找。    

### 使用规则
推荐 Windows 使用 [GitHub Desktop](https://desktop.github.com/). 相关的用法请自行研究，这里只给出 Linux 命令式。

#### git 的使用和仓库克隆同步

第一次使用 git 需要配置全局用户名和电子邮件。如果是 GH Desktop 会在第一次进入时自动设置：
```bash
git config --global user.name GitHub名称
git config --global user.email GitHub登录邮箱
```

使用 `git clone` 克隆本仓库的 `master` 分支：  
```bash
git clone -b master https://github.com/Yescafe/PCR_CarryOn
```
git 协议的 URL 没有测试，暂不确定可用性。  

请在每次**提交完之后**和修改**你的分支之前**，执行一次
```bash
git fetch origin master
```
以检查与远程仓库的 `master` 的同步情况。如果本机的代码落后于远程仓库，则需要继续使用
```bash
git pull origin:master
```
以完成与远程仓库的同步。  

#### 协作功能
GitHub 的协作功能没什么好说的。只有仓库的主人添加到协作列表里的 GitHub 用户才可 push 到本仓库。其他用户请参照[“公开规则”](#公开规则)中给出的 pull request 方法。

### 提交规则
在克隆完 `master` 分支后，完成对自己的分支（后文称“编辑分支”）的建立和推送：
```bash
git checkout -b hanlin
git push origin hanlin
```
使用
```bash
git branch
```
检查当前的工作所在的分支。**请确保在自己的编辑分支工作。**  

对内容进行修改后，在仓库的根目录执行
```bash
git status
```
检查仓库的修改状态。再执行
```bash
git add .
git status
```
完成对所有文件的跟踪。最后为所有跟踪的修改文件打上 commit: 
```bash
git commit
```
注意不要使用 `git commit -m`.  

#### commit 规则
使用 `git commit` 会打开文本编辑器，试系统和配置不同可能为 nano、vim、VSCode 等。各个编辑器的用法忽视。  

请按照下面的格式书写 commit：
```
提交者: 主要完成内容

- 描述1
- 描述2
- ...
```
如：
```
狗群主: 更新大量黑话

- 添加了大量的黑话内容，修改了一些错别字
- 修改了阵容中一些错误的配置
```
如使用 GH Desktop 可以很容易添加如上内容，因为下面有两个框。  

### 合并规则
*合并目前只由仓库主完成。*  

不同于写手，负责合并的编辑需要同步仓库的所有分支，合并的方式不用多说。  

### 公开规则
毕竟是挂在 GitHub 上开源，所以也没法约束大家的行为。只希望转载请著名出处。其他的遵循 MIT 协议。

#### 使用 pull request 完成提交
使用 GitHub 的 fork 功能完成对本仓库的贡献。  
也请严格遵照以上的提交规则来，完成后请将内容合并到本仓库的 `base-dev` 分支。  
