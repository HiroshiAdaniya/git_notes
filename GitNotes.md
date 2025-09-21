<h1># Git commands</h1>

*git init* - This is the first step to initialize a directory as a repository.
<h6>An important note to remember: when renaming a file or removing a file, use "git mv filename / git rm filename", rather than the usual way you have done it before. This helps clear the messages when you use *git status* which allows your changes to be committed much easier</h6>

<p>Without *git init* you are just working with a normal directory and the commands associated with *git* will not work. You won't be able to stage and commit changes to github</p>

<h2># What happens when you *git init*</h2>

<p>a ".git" file is created with all the configurations needed to create an environment to connect to github </p>

	* git init ---> Enter the directory you want to initialize
	* git init directoryName ---> creates and initializes the directory/repository

<h2># Configuring your environment: Setting username and email</h2>

	* git config --global user.name "user name"
	* git config --global user.email user@email.com

<h2># What is .gitignore</h2>

*.gitignore* is a file that contains all the files and details git should ignore


<h2># Environments in Git</h2>

There are 3 different environments in git:

***Working files***

<p>This environment allows you to make edits to files</p>
	
	* git status ---> Allows you to see if there were modifications made to the files in the directory /  repository
	* git diff ---> Allows you to see the actual changes made to a file or changes made between branches
	* git pull ---> This fetches updated code and content from the cloud so that you are up-to-date with everyone. Do it frequently.
***Staging***

<p>This is the holding stage, which allows you to save your progress so that when you ready you can send it off to github</p>

	* git add filename ---> Includes only the file you have added
	* git add -A / git add --all / git add . --> 3 different options you can choose from to add all files

	*git restore --staged filename --> removes the file/files you have just added

***Committing***

<p>This is where you push your changes to the cloud repository, which would be on github</p>

	* git commit -m 'a comment made about the commit' ---> This commit the changes you have made
	* git commit -a -m 'commit message' ---> allows you to skip the adding stage
	* git commit -m 'commit' --amend ---> Corrects the last commit you have made

***Resetting to a previous commit***

<p>"*--soft*" and "*--hard*" are only recommended if you are working a project alone. When working on a team project, use "*git revert*" </p>

	* git reset --soft commitCode ---> This allows you to go back to a certain commit you have made while still keeping the current changes you've made. It only changes the commit message and not the contents. You can find the "commitCode" by using **git log**.

	* git reset --hard commitCode ---> this does the exact same as '--soft' expect all the work you have done ater that point, will be lost. This resets the stage area to that particualr point. Future work will be deleted.

	* git revert commitCode ---> This will remove the change you have made but will still keep the commit message in the log. It will then create an addtional log with the update so that the team which is using the code will not run into any issues.

<h2># Additional commands</h2>

***log***

	* git log ---> This allows you to see all the commit you have made with their special identifiers/ code reference/ author / username/ user email/ date & time
	* git log --oneline ---> abbreviated version of git log
	* git log -p ---> Allows you to see a full detail description of the changes you have made
	* git log help ---> A manual for the log command

***Removing and Renaming***

	* git mv filename newfilename ---> Renames a file
	* git rm filename ---> Removes a file

***Jumping back to previous commits***

	*git reset "commit code/ reference" ---> This will set you back to the commit stage you want to be at. The commit codes can be found in git log

<h1># Branching</h1>

<p>Branching allows you to create a duplicate of the main/master environment you are working in. The purpose is to make changes that do not affect the main branch so when you are ready to merge the changes, you can. This allows multiple developers to work on the same code at different stages</p>

***Creating a branch***

	* git branch branchName ---> Creates a new branch
	* git switch -c branchName ---> creates and swicthes you to the new branch
	* git branch ---> Allows you to see a list of branches and highlights the one you are on

***Switching between branches***

	* git switch branchname ---> switch to a branch
	* git checkout branchname ---> essencially does the same as switch

***Merging branches***

	* git merge -m "merging comment" branchName ---> On the main branch, you merge with the changes from the branch you created
	* git merge branchName ---> merge branches without a commit message

<p>When merging branches you can run into merge conflicts where there were chanages o both the main and alternate branch. You can fix these merges by going into the file where there is conflict and choose the correct update. After you have resolved the conflict you can choose to commit them. </p>

***Deleting branches remotely and on github***

	* git branch -d BrachName ---> deletes the unwanted branch remotely
	* git push origin --delete branchname ---> deletes the branch from the cloud / github


