###修改用户名和邮箱命令分别为：
```
git config  --global user.name '' // 你的目标用户名

git config  --global user.email '' // 你的目标邮箱名

vi ~/.gitconfig
```

###撤回commit
git reset --soft HEAD^

--mixed 
意思是：不删除工作空间改动代码，撤销commit，并且撤销git add . 操作
这个为默认参数,git reset --mixed HEAD^ 和 git reset HEAD^ 效果是一样的。

--soft  
不删除工作空间改动代码，撤销commit，不撤销git add . 

--hard
删除工作空间改动代码，撤销commit，撤销git add . 

注意完成这个操作后，就恢复到了上一次的commit状态。

git commit --amend

此时会进入默认vim编辑器，修改注释完毕后保存就好了。




## 代码提交规范

commit 信息分类标准

* feat：新功能（feature）
* fix：修补bug
* docs：文档（documentation）
* style： 代码格式（不影响代码运行的变动）
* refactor：重构（即不是新增功能，也不是修改bug的代码变动）
* test：增加测试
* chore：构建过程或辅助工具的变动

**例如**  

bash.  
git add xxx   
git commit -m 'feat: 新增xxx功能 to #1234(aoneID)'.  
git commit -m 'fix: 修复xxx问题 to #1234(aoneID)'.  
git commit -m 'docs: 添加xxx文档/xxx文档更新'.  
git commit -m 'style: 代码风格调整'.  
git commit -m 'refactor: xxx函数逻辑重构'.  
git commit -m 'test: xxx功能添加测试'.  
git commit -m 'chore: webpack 打包模块升级'.  
