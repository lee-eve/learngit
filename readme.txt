Git is a version contril system.
Git is free software.
Come On Git.
LeanningGit : git add [file name];
	  git commit -m "log msg";
	  git status;
	  git diff; look some different 
	  git log; look  log
	  git reset --hard HEAD^;
	Git必须知道当前版本是哪个版本，在Git中，用HEAD表示当前版本，也就是最新的        提交3628164...882e1e0（注意我的提交ID和你的肯定不一样），上一个版本就是H        EAD^，上上一个版本就是HEAD^^，当然往上100个版本写100个^比较容易数不过来         ，所以写成HEAD~100。一大串类似3628164...882e1e0的是commit id（版本号）
	可以通过commit id来回到任何版本。
	  git reflog；Git提供了一个命令git reflog用来记录你的每一次命令 
	  git config --global user.name "yourname";
	  git config --global user.email "youremail@example";
	  ok
 
