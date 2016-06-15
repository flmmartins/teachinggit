# Git

## Diference between GIT & SVN

![GIT & SVN](http://techidiocy.com/wp-content/uploads/2013/08/svn-repo.png)
Source: techidiocy.com


## Git Steps

![gitsteps](http://codingdomain.com/git/partial-commits/git-staging-area.png)
Source: codingdomain.com

![gitstepsexample](https://lh3.googleusercontent.com/-j3nyobdTyBM/V2Fuzy3L57I/AAAAAAAAA30/U_XLNeqxVYk/w702-h414-p-no/Screen%2BShot%2B2016-06-15%2Bat%2B11.05.11%2BAM.png)

## Configuring yourself

```
git config --global user.name "John Doe"
```

```
git config --global user.email youremail@mai.com
```

##Creating a repo

```
git init

```

#### Checking status

```
git status
```
**Readme is always god**

Create a file README.MD. It will stay in **working directory**

```
git status
```

Add to **Staging Area**

```
git add README.md
```

```
git status
```

Add to **LOCAL Repository**

```
git commit -m "Initial Commit"
```

```
git status
```

Whats going on? Where are my changes?


#### Logging

```
git log
```

![simplelog](https://lh5.googleusercontent.com/-F13i0n7AV3s/V2FyXLM-gFI/AAAAAAAABXE/mSdRyQrvXQQ5sBKl49Q2hQNGyLTkhigAgCL0B/w1748-h1176-no/2016-06-15.png =600x400)

An Improved log:

```
git config --global alias.lg 'log --abbrev-commit --oneline --decorate'
```

![image](https://lh6.googleusercontent.com/-WT60iNH7GJU/V2F0IrzLT2I/AAAAAAAABXQ/syLMiEJQem0Bv4NUPoARbKrjY3NOO3_VQCL0B/w1882-h230-no/2016-06-15.png =600x75)

#### Ignore

Let's create a log file. 

```
git status
```

Do we want this in our repository? No. Let's add a .gitignore file

```
vim .gitignore
```

Adds the log file name or a regex to it

```
git add .gitignore
```

```
git status
```

Notice that the log file don't show up anymore. Commit it

```
git commit -m "My first gitignore"
```

```
git log
```

Now what?

#### Pushing to Remote Repository

First we need to set the remote:

```
git remote add origin <url.git>
```

```
git remote -v
```

![image](https://lh5.googleusercontent.com/-7HYXKoI0RGM/V2F3stxpikI/AAAAAAAAA4U/1kHIKTpwt_c_nRTfX-Ns1bGBGgCSbpRiACL0B/w1878-h302-no/Screen%2BShot%2B2016-06-15%2Bat%2B11.43.22%2BAM.png =600x)

Make the code available to everyone:

```
git push origin master
```

Where origin is the nickname of your remote and master is our current branch

Open the repository and check!

#### Cloning

If someone wants to colaborate ask then to clone

```
git clone git@github.com:flmmartins/teachinggit.git
```

```
git log
```


#### Diffing

Edit README.md file

Check diferences bettwen your README and repository README. You can only diff begore add

```
git diff README.md
```

Commit your code and push! Something went wrong? Update code first


#### Update the code

```
git pull --rebase
```
 
### Branch


Let's create a **local** branch

```
git checkout -b <branch name>
```

To check your local branches and where you are (check *)

```
git branch -v
```

Check you remote branches

```
git branch -r
```

Notice that your branch is not in the remote yet

Create a file and commit


```
git log
```

Let's take a look on master before we continue with our branch

```
git checkout master
```

```
git log
```
```
git checkout <your branch>
```

```
git push origin <your branch>
```

If you need to merge with you need to change to master and use $git merge <your branch>. But how about opening a Pull Request instead?



## Cheat Sheet
https://recompilermag.com/issues/issue-1/how-to-teach-git/










