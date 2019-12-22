# git
Git cat-file -t 58c9 // type
Git cat-file -p 58c9 // 内容 111

111 -> SHA1哈希算法 -> 58c9…

Git Object // blob 基本单位  git add
Tree Object // git commit
Git object:
	- blob: 文件内容
	- tree：目录结构/文件权限/文件名
	- commit：上一个commit/对应快照/作者/提交信息
	
	refs

Git 三个分区
- 工作目录
- 索引（暂存区）
- git仓库

技巧：
1. 误删除
	git reflog
2. 如何获得一个干净的工作空间
	以前：
	git reset —hard HEAD 或 git checkout -f
				git clean -df
	推荐：
	git stash push [-u | —include-untracked]
3. 从Git历史中删除一个文件
	git filter-branch —tree-filter ‘rm -f passwords.txt’ HEAD

Git commit —amend // 修补最近一次的commit message
git rebase -I origin/master // 修改还未push的所有commit内容
git show-branch // 
Git blame // 最后一次变更
git bisect // 二分法
