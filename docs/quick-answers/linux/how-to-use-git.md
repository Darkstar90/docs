---
author:
  name: Angel Guarisma
  email: aguarisma@linode.com
description: 'This Quick Answer guide explains how to use Git to create a repository, stage a commit, and then push that commit.'
<<<<<<< HEAD
keywords: ["Linux", " how to use Git", " github", " create git repo"]
aliases: ['quick-answers/how-to-use-git/']
license: '[CC BY-ND 4.0](https://creativecommons.org/licenses/by-nd/4.0)'
modified: 2017-07-17
modified_by:
  name: Angel Guarisma
published: 2017-06-19
=======
keywords: 'Linux, how to use Git, github, create git repo'
alias: ['quick-answers/how-to-use-git/']
license: '[CC BY-ND 4.0](https://creativecommons.org/licenses/by-nd/4.0)'
modified: 'Monday, July 17th, 2017'
modified_by:
  name: Angel Guarisma
published: 'Monday, June 19th, 2017'
>>>>>>> cfb4ddbda8a19130b6bbff342b53154dba398ac5
title: How to Use Git the Version Control System
external_resources:
- '[Learn Git with Bitbucket Cloud](https://www.atlassian.com/git/tutorials/learn-git-with-bitbucket-cloud)'
- '[Pro Git Book](https://git-scm.com/book/en/v2)'
- '[Github Guides](https://guides.github.com/)'
---

Git is a [version control system](https://en.wikipedia.org/wiki/Version_control) that can be used to manage software projects. This guide's six steps will show you how to initialize a Git repository, stage files for a commit, and commit these files to a local Git repository. For fuller instruction, refer to our more robust guide on [Git Source Control Management](/docs/development/version-control/how-to-install-git-on-mac-and-windows).

1.  Create a folder in which to store your files, then initialize a Git repository in that folder:

<<<<<<< HEAD
		mkdir testgit
=======
		mkdir testgit 
>>>>>>> cfb4ddbda8a19130b6bbff342b53154dba398ac5
		cd testgit
		git init

2. Create files for Git to track, then append some text to a file:

		touch file.txt file2.txt file3.txt
		echo "hello Linode" >> file.txt

3.  Use command, `git status`, to return information about the current Git repository:

		git status
		On branch master

		Initial commit

		Untracked files:
		 (use "git add <file>..." to include in what will be committed)
<<<<<<< HEAD

		file.txt
		file2.txt
		file3.txt

=======
  
		file.txt
		file2.txt
		file3.txt
				
>>>>>>> cfb4ddbda8a19130b6bbff342b53154dba398ac5
		nothing added to commit but untracked files present (use "git add" to track)

4. Since `file.txt`contains text, you want Git to track any future changes to that file. Use `git add file.txt` to add `file.txt` to the list of files Git monitors. Type `git status` after the addition to confirm that Git is tracking the new file.

		git add file.txt
		git status

<<<<<<< HEAD
	This will return:
=======
	This will return: 
>>>>>>> cfb4ddbda8a19130b6bbff342b53154dba398ac5

		On branch master

		Initial commit

		Changes to be committed:
		(use "git rm --cached <file>..." to unstage)
<<<<<<< HEAD

		new file:   file.txt

		Untracked files:
			(use "git add <file>..." to include in what will be committed)

=======
  
		new file:   file.txt
	  
		Untracked files:
			(use "git add <file>..." to include in what will be committed)
		
>>>>>>> cfb4ddbda8a19130b6bbff342b53154dba398ac5
			file2.txt
			file3.txt

5. To commit the changes of `file.txt` to the version control system, use `git commit`. Git requires you to write a commit message, a message will help you remember the changes you have made to your files. In this example, use the `-am` options to commit `a`ll modified files, specifically the ones Git is tracking, and include a commit `m`essage:

		git commit -am "Added Hello Linode to file.txt"

<<<<<<< HEAD
    Git will return the following message, confirming your new changes:

=======
    Git will return the following message, confirming your new changes:  
	
>>>>>>> cfb4ddbda8a19130b6bbff342b53154dba398ac5
		[master (root-commit) e8cc496] added new file
		1 file changed, 1 insertion(+)
		create mode 100644 file.txt

6. Track the remaining files in the directory using `git add -A`, and commit them with a message:

		git add -A
		git status
<<<<<<< HEAD

    Returns:

=======
    
    Returns:
    
>>>>>>> cfb4ddbda8a19130b6bbff342b53154dba398ac5
		On branch master
		Changes to be committed:
		(use "git reset HEAD <file>..." to unstage)

		modified:   file.txt
		new file:   file2.txt
		new file:   file3.txt

<<<<<<< HEAD
    Now, commit the changes:

        git commit -am "The end!"

        [master 52a9240] The End
        4 files changed, 1 insertion(+)
        create mode 100644 file1.txt
        create mode 100644 file2.txt
        create mode 100644 file3.txt

{{< note >}}
`git add -A`, `git add .`, and `git add -u` can all be used to stage files for a commit.
 `git add -A` stages `a`ll of the files in the directory. `git add .` stages only the new and modified files, omitting  any deleted files. `git add -u` stages only the modified and deleted files, omitting any new files.
{{< /note >}}
=======
   Now, commit the changes:

        git commit -am "The end!"

		[master 52a9240] The End
		4 files changed, 1 insertion(+)
		create mode 100644 file1.txt
		create mode 100644 file2.txt
		create mode 100644 file3.txt

{: .note}

>`git add -A`, `git add .`, and `git add -u` can all be used to stage files for a commit.
> `git add -A` stages `a`ll of the files in the directory. `git add .` stages only the new and modified files, omitting  any deleted files. `git add -u` stages only the modified and deleted files, omitting any new files.
>>>>>>> cfb4ddbda8a19130b6bbff342b53154dba398ac5
