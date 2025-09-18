# MY_PROJECT
2. 执行了 git submodule update --remote 命令，使子模块切换到指定的分支。从命令输出可以看到，子模块'gun'已成功检出到特定提交。
如果需要指定其他分支，只需将.gitmodules文件中的branch字段值改为所需的分支名，然后再次执行 git submodule update --remote 命令即可。

另外，如果是首次添加子模块，也可以在添加时直接指定分支： git submodule add -b 分支名 仓库地址 子模块路径
============================================================================
您可以使用Git子模块（Git Submodule）功能来实现这个需求。以下是具体步骤：

1. 1.
   创建新的主仓库
   
   - 在GitHub/Gitee等平台上创建一个新的空仓库
   - 克隆到本地： git clone 您的新仓库地址
2. 2.
   添加GUN和DONGLE作为子模块
   
   - 进入主仓库目录： cd 您的主仓库目录
   - 添加GUN子模块： git submodule add GUN仓库地址 gun
   - 添加DONGLE子模块： git submodule add DONGLE仓库地址 dongle
   - 提交更改： git commit -m "添加GUN和DONGLE子模块"
   - 推送至远程： git push origin master
3. 3.
   初始化和更新子模块
   
   - 克隆包含子模块的仓库时： git clone --recurse-submodules 您的主仓库地址
   - 已克隆主仓库后更新子模块： git submodule update --init --recursive
4. 4.
   同步子模块更新
   
   - 进入子模块目录： cd gun （或 cd dongle ）
   - 拉取最新代码： git pull origin main
   - 返回主仓库： cd ..
   - 提交子模块版本更新： git commit -am "更新GUN子模块至最新版本"
   - 推送至远程： git push origin master