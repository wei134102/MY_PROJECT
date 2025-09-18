# MY_PROJECT
2. 执行了 git submodule update --remote 命令，使子模块切换到指定的分支。从命令输出可以看到，子模块'gun'已成功检出到特定提交。
如果需要指定其他分支，只需将.gitmodules文件中的branch字段值改为所需的分支名，然后再次执行 git submodule update --remote 命令即可。

另外，如果是首次添加子模块，也可以在添加时直接指定分支： git submodule add -b 分支名 仓库地址 子模块路径