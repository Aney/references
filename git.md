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

or

    git clone https://github.com/USER/REPO

# Commit new changes to the repository

Add the new file, or the changed file/directory

    git add file

Commit with a message; What and why was it changed

    git commit -m 
