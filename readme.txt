Git is a version contril system.
Git is free software.
Creating a new branch is quick.
Come On Git.

test confilct
>>>>>>> feature1

LeanningGit :
	 1. git add [file name];
	 2. git commit -m "log msg";
	 3. git status;
	 4. git diff; look some different 
	 5. git log; look  log

	 6. git reset --hard HEAD^;
	Git必须知道当前版本是哪个版本，在Git中，用HEAD表示当前版本，也是最新的        提交3628164...882e1e0（注意我的提交ID和你的肯定不一样），上一个版本就是H        EAD^，上上一个版本就是HEAD^^，当然往上100个版本写100个^比较容易数不过来         ，所以写成HEAD~100。一大串类似3628164...882e1e0的是commit id（版本号）
	可以通过commit id来回到任何版本。

	 7. git reflog；Git提供了一个命令git reflog用来记录你的每一次命令 
	 8. git config --global user.name "yourname";
	 9. git config --global user.email "youremail@example";
	  ok 我有了一个分布式的版本控制在Github上、；

 	 10. Git鼓励大量使用分支：
	  查看分支：git branch；
	  创建分支：git branch <name>
	  切换分支：git checkout <name>
	  创建+切换分支：git checkout -b <name>
	  合并某分支到当前分支：git merge <name>
	  删除分支：git branch -d <name>

	 11.当Git无法自动合并分支时，就必须首先解决冲突。解决冲突后，再提交，		  合并完成。
	     git log --graph命令可以查看到分支合并图。

	 12.分支策略：
		在实际开发中，我们应该按照几个基本原则进行分支管理：首先，master                分支应该是非常稳定的，也就是仅用来发布新版本，平时不能在上面干活                ；那在哪干活呢？干活都在dev分支上，也就是说，dev分支是不稳定的，                到某个时候，比如1.0版本发布时，再把dev分支合并到master上，在mast                er分支发布1.0版本；你和你的小伙伴们每个人都在dev分支上干活，每个                人都有自己的分支，时不时地往dev分支上合并就可以了。  	   
