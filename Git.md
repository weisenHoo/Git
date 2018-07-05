###Linux常用命令
>- 创建文件夹：midir <file>
>- 创建文件：touch <file>
>- 显示文件列表：ls
>- 显示隐藏文件列表：ls -a
>- 删除文件：rm -rf * (慎用)
>- 打开文件编辑：vim <file>
>- -> 编辑：i
>- -> 保存：w
>- -> 退出：q
>- 查看文件内容：cat <file>

###使用系统别名定义git全局指令
>- 修改：.bash_profile文件(路径：'/User/.bash_profile')
```
alias gs="git status"
alias gc="git commit -m"
alias gl="git log --graph --pretty=format:'%Cred%h%Creset -%C(yellow)%Creset %s %Cgreen(%cr)'"
alias gb="git branch"
alias ga="git add ."
alias go="git checkout"
```

#Git命令
>- 初始化：git init
>- 查看文件状态：git status
>- 添加到索引库：git add <file>
>- 移除文件：git rm <file>
>- 从版本库中移除文件：git rm --cached <file>
>- 修改文件名字：git mv <file> <file>
>- 文件 .gitignore ：排除不需要推送的文件

###撤销
>- 撤销：git rm --cached <file>
>- 撤回：git checkout -- <file>

###提交
>- 推送到版本库：git commit -m '日志'
>- 修改推送描述：git commit -amend

###日志
>- 查看日志信息：git log
>- 查看变动信息：git log -p
>- 查看精简信息：git log --oneline
>- 查看精简变动信息：git log --oneline -p
>- 查看文件变化信息：git log --name-only
>- 查看文件变化类型信息：git log --name-status

###分支
>- 查看分支：git branch
>- 查看远程分支：git branch -a
>- 创建分支：git branch name
>- 切换分支：git checkout name
>- 创建分支并切换：git checkout -b name
>- 合并分支：git merge name
>- 删除分支：git branch -d name
>- 强制删除分支：git branch -D name (慎用)
>- 查看已经合并的分支：git branch --merged
>- 查看没有合并的分支：git branch --no-merged

###临时储存
>- 临时储存：git stash
>- 查看暂存区文件列表：git stash list
>- 恢复暂存文件：git apply (默认恢复最近一次修改)
>- 删除暂存区文件：git stash drop stash@{0}
>- 恢复并删除暂存文件：git stash pop
>- 恢复单个暂存文件：git stash apply stash@{1}

###添加标签
>- 添加标签：git tag v1.0

###打包生成压缩文件
>- 压缩：git archive master --prefix='hdcms/' --forma=zip > hdcms.zip

###移动分支节点
>- 移动主分支节点：git rebase master

###生成SSH秘钥
>- 生成秘钥：ssh-keygen -t rsa

###推到远程
>- 推送：git push

###关联github
>- 关联：git remote add origin git@github.com:weisenHoo/test.git
>- 取消关联：git remote remove origin
>- 推送：git push -u origin master

###修改配置
>- git config --global user.name "weisen"
>- git config --global user.email "306429737@qq.com"
>- git config --global alias.a add
>- 注：--global 设为全局

###克隆项目
>- git clone https://github.com/houdunwang/cart.git

###删除缓存数据
>- 查找 known_hosts 文件，删除文件里的内容
