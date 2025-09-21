<h1># Merge Conflicts</h1>

<h3># What is a merge conflict?</h3>

<p>A merge conflict is an event that happens when Git is unable to resolve difference in code between two commits.

For example, if you or a team member makes changes to a file on the ***Main/Master*** branch called ***index.html*** but you've already created a separate branch before the changes were made, once you're done editing the file ***index.html*** and try to merge it to the branch, you'll run into a ***merge conflict*** </p>

<p>There are two kinds of merge conflicts
	
	* remote branch merges
	* push conflicts (github)
</p>

<h3># How to resolve remote branch merge conflicts?</h3>

<p>Open the file/file's where the merge conflicts are taking place and manually choose the correct changes made to it.

After editing, use the ***git add*** command to stage the new merge and follow up with the ***git commit*** command.</p>

<h3>Git commands to resolve conflicts</h3>

	* git log --merge ---> Lists the commits that are causing the conflict
	* git diff ---> See the difference between the files or repositories/branches
	* get checkout ---> Allows you to undo the changes made to a file or to switch branches
	* get checkout ---> It will return a message with the files that are conflicted. It allows you to undo the changes made to a file or to switch branches.
	* git reset --mixed ---> This is used to undo the changes made in the current working directory and staging area
	* git merge --abort ---> Exits our of the merging process and returns back to the oint before the merging began
	* git reset ---> This will return the files back to their original state before there was a conflict. The current work will be lost

<h3># How to resolve push conflicts from github</h3>

<p>When you try and push your commits to github and you receive a merge conflict, your first step is to pull</p>

<p>1) You'll need to do a pull request to compare your changes</p>

	* git pull --rebase origin branchname

<p>2) Once that is completed you'll be returned a message detailing the conflicts. You'll need to resolve them with a mergetool</p>

	* git mergetool

<p>3) Once you've manually resolved the issues, next you'll need to continue...</p>

	* git rebase --continue

<p>4) Finally push your changes to the serve and you're done</p>

	* git push

# end

