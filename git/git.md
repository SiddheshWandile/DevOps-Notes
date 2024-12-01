# Git Notes

Git is one og the most famous version control system. Using git we can manage multiple version of a project and enable collabrative environment for multiple people working on the same project.

## How to get started with git?

To make sure that a projects version is controlled by git, we need to enable git inside that project. How to do it?

```bash
git init
```

The moment we execute git init. git initialises a project named as `.git` int the project directory and them every version control relation will be done using this `.git` folder.
Make sure you execute a command in the root directory of the project you want to track.

## How git maintains 3 areas for tracking changes to a file.

1. Working Area
2. Staging Area
3. Repository Area

## Working Area

Any file that is already being track `.git` some modification, then this new changes are kept in the working area region. These are mainly new changes are kept in the working area region. These are mainly new chnages in exixting git project.
if we want to move a changes from working area to staging area we can do

```bash
git add file name
```

The git add command will help you to add the changes form working area to staging area. We can add multiple files together by giving their name space seprated, or we add thr files of the current project form working area to staging area by doing.

```bash
git add .
```

## Staging Area

Here we have those changes which are going to be part of the next version, but are not yet in the next version.
If we want to move the content form staging area to repository area by making a commit we can use `git commit` command.

```bash
git commit -m "some massage"
```

With this command all the files in staging area become part of a new version.

### Note

In the world as git version / checkpoint is also referred as commit.

## Repository Area

Here we have those chnages which are already part of some earlier version.

### Note:

1. if we create a brand new file in a project. then by default that file is in a untracked statge. To start traking the file, we can `git add fileName`, this will not just start file tracking but with the current content of the file, add that file in the staging area directly.
2. There can be a case that we have some changes of a file in tge staging area, and some changes inn the workng area and some changes already in the repository area.
   This can happen when we have a file who is added in the staging area already, but before we add it to the next version, we made more changes to the file. These new changes are now part of working directory.

## How to check status about different areas?

So git provites a status command using which we can see what is the current status of chnages in working and staging area. All thr repository area chnages which are now a version, can be looked using `log` command.

```bash
git status
```

## How to enable collaborative coding with git?

Currently the project managed by git is in our locak machine, we need to put this project in a place where other can access. it. We can try to put it in a remote repository on the internet which is visible to other. And to this we can use `Github, GitLab, Bitbucket` etc.
These are online platform which allow you to host a remote repository(public or private) on their server. If the repository is public anyone can access, else for private ones, only people with an invite can acces it.

## How to upload our local repo on github?

So, we need to make sure that we are uploding out local repository on the git repository. To do this :

1. Setup a github account
2. Create a new Repo on github
3. We need to attach this new remote repo link to our local project. We can do that by `git remote ` command. git remote will help us to store this remote repository link in our project, give a name to it also, so that we can later use this remote link to uplode out changes.
4. We can use the `git push` command to upload thr changes.

```bash
git remote add origin ***link****
git push origin main
```

While doing git push, we need to mention name of the remote repo, here which is origin beacaus there can be multiple repo attahed to a local project.
To attach a new remote, we can use the `git remote add ` command and give a name to the remote also. Here origin is just a name to the remote repository link. We can even pick another name.

Everything that we have new in our repository area is uploaded to github once we push.

## How often should we create a commit / version and push it?

Everytime, you feel you have added some significant code, you should commit. otherwise may be you will loose it.

## Hoe to download latest changes made to the remote repository?

let's say some collabrator to your project added some code on the remote repository and you want sync your local repositroy with the new chnages, for doing this need to download the repository changes. We can do it using thr `git pull` command.

```bash
git pull origin main
```

Here we have added origin because we need to tell which remote repositroy should be consider for downloading the latest changes.

## How internally git workes?

1. Hashing
2. Graph / Tree Data Structure

git is like a key value store.
Key -> Hash of the data
value -> data

git uses a cryptographic hash function -> SHA1
for a given data, it output 40 digit hexadecimal number and the hash value is always same for same data.
git compresses a data in a blob and stores some metadata about data.
