If you are seeing this, that means the persistence is working!


This repository contains two applications:

1. **java-app** - A basic Java application.
2. **java-maven-app** - A Java application built with Maven.

If you encounter this issue: If you can NOT access the contents if your uploaded files in GitHub then the files may have been added as submodules instead of regular files or folders. So to upload the actual contents here are some steps to follow:

Step 1. run the following command/s to unstage and remove the submodules.
	git rm -- cached java-app (your file name)

That removes the submodules from your repository while keeping the files on your local machine.

Step 2. Remove .git Directories in Subfolders
	rm -rf java-app/.git (your file name/.git)

This step ensures that java-app (your file name) are treated as regular directories instead of Git repositories.

Step 3: Re-add the directories and commit them
	git add java-app java-maven-app
	git commit -m "Your description"

Step 4: Push the changes
	git push origin master (or main, or whatever branch you have designated)

	*If you want to make sure you are using the correct branch, type git branch*

