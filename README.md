# Cheat sheet for git commandline

This sheet is created for people that just start out with the git command line.
The bare basics to use git and get you quickly started and integrated with git.

### Create local a new branch
```
git checkout -b branchName
```

### Publish your local branch
```
git push --set-upstream origin branchName
```

### Upload your changes to your current branch

```
git commit -am 'tell about your changes'
git push
```

When you have created new files the following one is required.
```
git add .
git commit -m 'tell about your changes'
git push
```

### Get your local branches
```
git branch
```

### Update your local branch with online *(origin)* branch
```
git pull
```

### Update your local branch with an other online *(origin)* branch
```
git pull origin otherBranchName
```

### Create a tag

1. Get the recent commits
```
git log --pretty=oneline
```
Output will look like this:
```
commithash (HEAD -> currentBranchName, origin/currentBranchName) commit message
commithash commit message
commithash (tag: example-commit-that-has-tag) commit message
commithash commit message
```
Copy the `commithash` of the commit you want to give a tag.  

2. Create the tag.  
To bind the tag with a commit you paste the coppied `commithash`  
On the place where `commithash` stands in the following line:
```
git tag -a tag-name commithash
```

3. Publish the tag
```
git push origin tag-name
```



