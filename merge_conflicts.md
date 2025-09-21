<h1># Merge Conflicts</h1>

<h3># What is a merge conflict?</h3>

<p>A merge conflict is an event that happens when Git is unable to resolve difference in code between two ***commits***.

For example, if you or a team member makes changes to a file on the ***Main/Master*** branch called ***index.html*** but you've already created a separate branch before the changes were made and you then start to edit the same file ***index.html*** on the additional branch, once you switch to the ***main/Master*** branch and try to merge the two branches, you'll run into a ***merge conflict*** </p>

<h3># How to resolve merge conflicts?</h3>

<p>Open the file/file's where the merge conflicts are taking place and manually choose the correct changes made to it.

After editing, use the ***git add*** command to stage the new merge and follow up with the ***git commit*** command.</p>

<h3>Git commands to resolve conflicts</h3>

	* git log --merge ---> Lists the commits that are causing the conflict
	* git diff ---> See the difference between the files or repositories/branches
	* get checkout ---> Allows you to undo the changes made to a file or to switch branches
	* git reset --mixed ---> This is used to undo the changes made in the current working directory and staging area
	* git merge --abort ---> Exits our of the merging process and returns back to the oint before the merging began
	* git reset ---> This will return the files back to their original state before there was a conflict. The current work will be lost


