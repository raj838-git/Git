# Git
## _Git Basic Concept and Uses_

[![N|Solid](https://cldup.com/dTxpPi9lDf.thumb.png)](https://nodesource.com/products/nsolid)


### Git Configuration And Initialization 

Configure User name -
```bash
git config --global user.name Raj838
```

Configure Email Id -
```bash
git config --global user.email rajpankaj838@gmail.com
```

Check & See Configuration -
```bash
git config --global user.name
```
> Note: `--global` is required when you set user name and email as globally i.e. for whole PC. If we remove this argument than user name and email set only in present directory.

Git Initializing -
```bash
git init
```

Check Git Status -
```bash
git status
```
It show all Untracted & Modified file.

## Basic Concept of Git -
Git is a version control system. It is save changes of Staged file when it Commit usning taking Shanpshots of Changes.
#### WorkFlow - 
When we initialiazing git then it create Branch automatic. It is Main Branch and Name is **master**. And save Commits point respectively.
![image](https://drive.google.com/uc?export=view&id=1u2xaYnAAr4kqQgITDes6OnbFl21rQTa3)

After git initialiazing "git status" show Untracked & Modified file then we Staged these file and Commit to save Unmodified.

![image](https://drive.google.com/uc?export=view&id=10Fog2JVuNRxBj205C1vum87H734AoEd6)

## Basic Usages -

Staged a single file -
```bash
git add file_name
```

Staged all file -
```bash
git add -A
```

UnStaged A single File -
```bash
git reset file_name
```

UnStaged All file -
```bash
git reset
```

Commit -
```bash
git commit -M "first commt"
```

Show Git Commit History -
```bash
git log
```

Clone A Repository -
```bash
git clone Repository_link
```
Repository_link end with ".git" extension.
##### Push & Pull Repository Using Https :-
> Time to time Github change it security system due to which you may face some difficule during verification. May be it include some extra step for verification so check Github Official page.

Set/Add Remote Origin -
```bash
git remote add origin https://github.com/raj838-git/Test.git
```

Remove Remote Origin -
```bash
git remote remove origin
```

Push Repository -
```bash
git push -u origin master
```
> Note: `-u` is required only when we want to save current branch to pull automatically file from current branch to Remote server from next time.

#### Push & Pull Repository Using SSH :-
For pushing and pulling repository using ssh we need to configure ssh service first than Use following step :

Set Remote Origin -
```bash
git remote add origin git@github.com:raj838-git/Test.git
```

Remove Remote Origin -
```bash
git remote remove origin
```

Push Repository -
```bash
git push -u origin master
```

Pull Repository -
```bash
git pull origin master
```


## SSH Configuration -

Generate SSH key -
```bash
ssh-keygen -t ed25519 -C "your_email@example.com"
```

Start ssh-agent in background -
```bash
eval "$(ssh-agent -s)"
```

Add SSH-key to ssh-agent -
```bash
ssh-add ~/.ssh/id_ed25519
```
If you Use Passphrase Then Use give below Command to Add SSH-key to ssh-agent -
```bash
ssh-add -K ~/.ssh/id_ed25519
```
> Note:  `-k` is required when you use passphare during generating ssh-key otherwise you use command without `-k`.

Add SSh-key on github Account :-
For full description check git page.

## Advanced Uses:-

Check Differences B/w to Files -
```bash
git diff file_name
```

Check Differences B/w Staged File and Last Commit File -
```bash
git diff --staged file_name
```

Goto Previous Commit (file) -
First you Unstaged file if you Staged than Use following command :
```bash
git checkout file_name
```
> Note: `file_name` is required when you use a specific file otherwise you use all command without `file_name`. It is apply on all files.
```bash
git checkout .
```
It restore all files.

##### Ignore File from git -
first of all you create a ".gitignore" file:
```bash
touch .gitignore
```
Now add file Name, extension and Directory in .gitignore file :
```bash
nano .gitignore
```
It is edit .gitignore file in Terminal.
> Note: Git show `.gitignore` file as an untracked file so we tracked and commit it.

![image](https://drive.google.com/uc?export=view&id=1LTiiHpgKo0MZxRlQIAnXDNu5KHvY664s)

Ignore Previously Track file -
First you remove previous Track data Using following command and add file name in .gitignore file :
```bash
git rm --cached file_name 
```

##### Branches in Git -
When we initialiazing git then it create a Branch automatic. It is Main Branch and Name is **master**. And save Commits point respectively.
![image](https://drive.google.com/uc?export=view&id=1u2xaYnAAr4kqQgITDes6OnbFl21rQTa3)

But Some time we want to add another Features also and we want it not disturb main branch. So that we Create a another Branches. It is just clone **master** branch i.e. All files present in **master** also present in New Created Branches like :

![image](https://drive.google.com/uc?export=view&id=1bBKwzEAE10xQKh7KRElzcj5D7YRGm3El)

If New Feature is work proper than we want merge this Features in **master** branch like :

![image](https://drive.google.com/uc?export=view&id=1pN7hkrYWeCckzp0uSLx7y_ocaNCINVFF)

If New Feature is Not working proper or Afer merging branch to **master**, we want delete this branch like :

![image](https://drive.google.com/uc?export=view&id=1SsM1x_avpXh8JT4PO93rvXMnYrj3l_5T)

Check list of Branch and Active Branch -
```bash
git branch
```
> `Active Branch` contain a star like this  `*`

Create a Branch -
```bash
git branch branch_name
```

Change Active Branch -
```bash
git checkout branch_name
```

Push Repository on Remote server -
```bash
git push origin branch_name
```

Merage a Branch in **master** Branch -
First Go to **master** Branch Using Active branch command then use following command :-
```bash
git merge branch_name
```

Delete A Branch Locally -
```bash
git branch -d branch_name
```

Delete A Branch on Remote server -
```bash
git push origin --delete branch_name
```

## License

MIT

**Basic Guidelines For Git**

This is a [Github] project.
This is a [github](www.github.com) project.

[//]: # (These are reference links used in the body of this note and get stripped out when the markdown processor does its job. There is no need to format nicely because it shouldn't be seen. Thanks SO - http://stackoverflow.com/questions/4823468/store-comments-in-markdown-syntax)

   [Github]: <https://github.com>
   
