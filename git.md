# Create a GitHub repository and setup with terminal
Initialise the local repo
	git init
Add a file to the repo, in this case the file was "git"
	git add git
Commit to the repo, with a message
	git commit -m "Commiting the empty repository to GitHub"
Add the local repo to the GitHub repo
	git remote add origin https://github.com/SirAney/references.git
Push the commits from the local repo to the GutHub repo
	git push -u origin master

# Pull a repo from GitHub to local machine
	git init
	git pull http://github.com/USER/REPO

# Commit new changes to the repository
	git add file
	git commit -m 
