Git is a version contril system.
Git is free software.
Creating a new branch is quick.
Come On Git.
test conflict1.
LeanningGit :
	 1. git add [file name];
	 2. git commit -m "log msg";
	 3. git status;
	 4. git diff; look some different 
	 5. git log; look  log
	 6. git reset --hard HEAD^;
	Git必须知道当前版本是哪个版本，在Git中，用HEAD表示当前版本，也就是最新的        提交3628164...882e1e0（注意我的提交ID和你的肯定不一样），上一个版本就是H        EAD^，上上一个版本就是HEAD^^，当然往上100个版本写100个^比较容易数不过来         ，所以写成HEAD~100。一大串类似3628164...882e1e0的是commit id（版本号）
	可以通过commit id来回到任何版本。
	 7. git reflog；Git提供了一个命令git reflog用来记录你的每一次命令 
	 8. git config --global user.name "yourname";
	 9. git config --global user.email "youremail@example";
	  ok 我有了一个分布式的版本控制在Github上；
 	 10. Git鼓励大量使用分支：
	  查看分支：git branch；
	  创建分支：git branch <name>
	  切换分支：git checkout <name>
	  创建+切换分支：git checkout -b <name>
	  合并某分支到当前分支：git merge <name>
	  删除分支：git branch -d <name> 	   
