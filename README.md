#Git is a version contril system.
#Git is a free software.
#Creating a new branch is quick.
#Come On Git.

##LeanningGit :
	 1. git add [file name];
	 2. git commit -m "log msg";
	 3. git status;
	 4. git diff; look some different
	 5. git log; look  log
	 6. git reset --hard HEAD^;
		Git必须知道当前版本是哪个版本，在Git中，用HEAD表示当前版本，也是最新的        
		提交3628164...882e1e0（注意我的提交ID和你的肯定不一样），上一个版本就是
		HEAD^，上上一个版本就是HEAD^^，当然往上100个版本写100个^比较容易数不过来，
		所以写成HEAD~100。一大串类似3628164...882e1e0的是commit id（版本号）
		可以通过commit id来回到任何版本。

	 7. git reflog；Git提供了一个命令git reflog用来记录你的每一次命令 
	 8. git config --global user.name "yourname";
	 9. git config --global user.email "youremail@example";
 	 10. Git鼓励大量使用分支：
		查看分支：git branch；
	  	创建分支：git branch <name>
	  	切换分支：git checkout <name>
	  	创建+切换分支：git checkout -b <name>
	  	合并某分支到当前分支：git merge <name>
	  	删除分支：git branch -d <name>

	 11.当Git无法自动合并分支时，就必须首先解决冲突。解决冲突后，再提交,合并完成。
	     	git log --graph命令可以查看到分支合并图。

	 12.分支策略：
		在实际开发中，我们应该按照几个基本原则进行分支管理：首先，
		master分支应该是非常稳定的，也就是仅用来发布新版本，平时不能在上面干活;
		那在哪干活呢？干活都在dev分支上，也就是说，dev分支是不稳定的，                
		到某个时候，比如1.0版本发布时，再把dev分支合并到master上，在master分支
		发布1.0版本；你和你的小伙伴们每个人都在dev分支上干活，每个人都有自己的分支，
		时不时地往dev分支上合并就可以了
	       
	 13.关联远程库
		要关联一个远程库，使用命令git remote add origin git@server-name:path/repo-name.git；
		关联后，使用命令git push -u origin master第一次推送master分支的所有内容；此后，每次
		本地提交后，只要有必要，就可以使用命令git push origin master推送最新修改；  	
	   	要克隆一个仓库，首先必须知道仓库的地址，然后使用git clone命令克隆。Git支持多种协议，
	   	包括https，但通过ssh支持的原生git协议速度最快。
		要关联一个远程库，使用命令git remote add origin git@server-name:path/repo-name.git；关联后，
		使用命令git push -u origin master第一次推送master分支的所有内容；
		此后，每次本地提交后，只要有必要，就可以使用命令git push origin master推送最新修改；  	
	   	要克隆一个仓库，首先必须知道仓库的地址，然后使用git clone命令克隆。
	   	Git支持多种协议，包括https，但通过ssh支持的原生git协议速度最快。
	  
	  14.Bug分支
		存储当前工作现场：  git stash
		查看存储的工作现场： git stash list
		恢复工作现场：一是用git stash apply恢复，但是恢复后，stash内容并不删除，你需要用git stash drop来删除；
		另一种方式是用git stash pop，恢复的同时把stash内容也删了修复bug时，我们会通过创建新的bug分支进行修复，
		然后合并，最后删除；当手头工作没有完成时，先把工作现场git stash一下，然后去修复bug，修复后，再git stash
		pop，回到工作现场。
		
	  15.feature分支
		开发一个新feature，最好新建一个分支；如果要丢弃一个没有被合并过的分支，可以通过git branch -D <name>强行删除。

	  
	  16.多人协作
		多人协作的工作模式通常是这样：
		首先，可以试图用git push origin branch-name推送自己的修改;如果推送失败，则因为远程分支比你的本地更新，需要
		用git pull试图合并；如果合并有冲突，则解决冲突，并在本地提交；没有冲突或者解决掉冲突后，再用git push origin
		branch-name推送就能成功！如果git pull提示“no tracking information”，则说明本地分支和远程分支的链接关系没有
		创建，用命令git branch --set-upstream branch-name origin/branch-name。这就是多人协作的工作模式，一旦熟悉了
		就非常简单。

	小结
	查看远程库信息，使用git remote -v；本地新建的分支如果不推送到远程，对其他人就是不可见的；
	从本地推送分支，使用git push origin branch-name，如果推送失败，先用git pull抓取远程的新提交；
	在本地创建和远程分支对应的分支，使用git checkout -b branch-name origin/branch-name，本地和远程分支的名称最好一致；
	建立本地分支和远程分支的关联，使用git branch --set-upstream branch-name origin/branch-name；
	从远程抓取分支，使用git pull，如果有冲突，要先处理冲突。
