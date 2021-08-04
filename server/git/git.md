# Git Server

`su -` Switch to root for most of this

## Make a git user

`adduser git` 

Adduser if prefered to useradd, but in case

`useradd git`
`mkdir /home/git`
`chown -R git:git /home/git`

## Make the git directory
`mkdir /srv/git` This can got anywhere, but this makes sense
`cd /srv/git`

### Give ownership of the directory
`chown -R git:git /srv/git`

## Add a repo
`git init --bare <repo>`


## How to clone, commit, etc. from your server

### Add existing branch
Add remote to existing Repo
`git init`
`git remote add <origin> ssh://git@<host>:<port>/srv/git/<repo>` \*
`git push (--set-upstream/-u) <origin> <branch>` 

### \* Remove the port
Don't use the <port>! You don't need to if your port is 22 (default ssh).
If you've changed it to be more secure, then instead change your ssh config!!

`.ssh/config` add

    Host <host>
        Port <port>

### Clone the branch
Clone is the same, but with `git clone`, not `git remote add <origin>`

## Add SSH keys

As the git user! 
`su git` if you're still logged in as root :)

Either ssh-copy-id from your PC, connecting to the server as git@<server>.
Or
Make an authorised keys file and add keys manually
`mkdir .ssh && chmod 700 .ssh`
`touch .ssh/authorized_keys && chmod 600 .ssh/authorized_keys`
Then copy keys into `.ssh/authorized_keys`
