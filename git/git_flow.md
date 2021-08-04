# Git Flow 

This can be done with the git-flow extension, or without.
All examples here, are with a from scratch repo.

## Initialised

git init
git flow init

## Main/Develop

After commiting a basic README.md to the main branch

    git checkout -b develop

The develop branch is where development work will be based off.

Don't work on the main/master branch.

## Feature Branch

This is where you work on features, changes, fixes\*, etc.

The develop branch will have many features, and can be by different developers

### Starting a feature branch

    git checkout develop
	git checkout -b feature/featureName develop

    git flow feature start featureName develop

#### Working on feature

You work on feature branch like normal, just do you development, and commit changes. When the feature is complete, you merge it into the development branch.

### Finishing a feature branch

    git checkout develop
	git merge --no-ff feature/featureName

    git flow feature finish featureName

### After feature finished

Your other features will need to be rebased onto the new develop branch.

    git checkout feature/anotherFeature
    git rebase develop

This can be done upon completion of the feature if you don't need anything from other features.

## Release Branch

Once a release is ready (all features for the upcoming release are complete). Then a release branch is created ready to roll out.

Release branches follow semantic versioning. Major|Minor|Fix.

### Starting a release branch

    git checkout develop
    git checkout -b release/0.1.0

    git flow release start 0.1.0

It might be worth pushing the release branch so it can be pulled and worked on by others.

    git push --set-upstream origin release/0.1.0

#### Working on release branch

If the release is staged, ready to go, but not ready to be live yet, then this is where bugfixes, etc are applied.

You will also want to change anything refering to the versin number, and rebuild caches, etc. before releasing.

### Finishing a release branch

    git checkout main
    git merge --no-ff release/0.1.0

    git flow release finish

Make sure to push tags too

    git push origin --tags

## Hotfixes

I've not got here yet

