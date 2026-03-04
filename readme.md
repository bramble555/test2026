创建分支:
git branch branch_name
切换分支:
git switch branch_name

公司操作流程:
1.git clone url
2.git checkout master
3.git pull origin master
4.git checkout -b feature/user-login-auth  # 分支名通常带 feature/ 前缀
5.git add .
6.git commit -m "feat: add jwt token verification logic"
7.git push -u origin feature/user-login-auth
7. 进阶：大厂常遇到的两个“坎”
场景 A：代码冲突了（Conflict）
如果你开发了一周，合入时发现 master 已经变了，MR 提示冲突。

做法： 你需要在本地切回 master，pull 最新代码，然后回到你的分支执行 git rebase master 或 git merge master。解决完冲突后再 push。

场景 B：提交太碎了（Squash）
如果你一个功能 commit 了 20 次，导师会让你“压减提交”。

做法： 使用 git rebase -i HEAD~n 将多个无意义的 commit 合并成一个整洁的提交
神经对啊,我就算神经病

