## Before We Start

All `git` commands will be run in the command line eg: `Command Prompt` or `Powershell` on Windows, `Bash` on Linux, etc. 
- If on Windows
	1. Install `Windows Terminal` from the Microsoft Store
	2. Run `Powershell` from the `Windows Terminal`

You will also need a Github Account to work with `git`. If you have not made one, create an account at `https://github.com/`.

#### Terminologies

| Word | Definition |
| --- | --- |
| Repo | Short for repository. It is a location where <br> source code and related files are stored <br> and managed in a version control system |
| Local Repo | This is the repository stored in your computer |
| Remote Repo | This is the repository stored in the cloud eg: `Github` |

#### Command Line Arguments

Arguments are what we pass on to command line programs like `git` in order for them to work based on user input. 

Now let's discuss the difference between a string literal and a placeholder. If we have an argument `path` then that is the string literal `path`, if we have an argument `<path>` then that is a placeholder and it could mean any path.

Example:
- `git path` literally means `git path`. On the other hand, `git <path>` could mean `git D:\Documents\Downloads` or any other path.
- `git file` literally means `git file` however `git <file>` could mean `git myfile.txt` or `git Main.java` or any other file

If a placeholder ends with an ellipsis (`...`) like `<files...>` then that means it can accept multiple arguments of that type.

Example:
- `git add <files...>` could be `git add test.txt` or `git add myfile.txt test.txt` or `git add Main.java Log.java config.txt` and so on.

#### Configuring Git

1. In the command line, run `git config --global core.editor "<path>"` where `<path>` is the absolute path to your text editor's executable file
	- If you have `Visual Studio Code` installed, run `git config --global core.editor code`
2. Run `git config --global --edit`. This will open the `.gitconfig` file on your designated text editor.
3. In the `[user]` section, check if the `name` and `email` is the same with your github account.
4. In the `[init]` section, change `defaultBranch` value to `main`
5. Finally, in the `[core]` section, change `safecrlf` value to `false`

## Creating Remote Repo

1. Go to `https://github.com/` in the web browser of your choice
	- Sign in or register if you have not
2. Click your profile and go to `Your repositories`
3. Click `New`
4. Fill in the information

## Initialize Local Repo

Once the remote repo has been created.
1. In the command line, go to your project's root directory and run `git init`
2. Go to the repo you created in `https://github.com/` and get the URL of the repo.
3. Connect local repo to remote repo with `git remote add origin <url>` in the command line.

## Commiting

#### Staging Area

This is where you will setup the files you want to commit.
1. To see files that have been changed, run `git status`
2. Stage files that you want to commit with `git add <files...>`
	- Use `.` to add all files

#### Commit The Changes

Once the files you want to commit have been staged.
1. Run `git commit -m "<message>"`
	- Always try to give your commits a simple and concise message.

## Pushing Changes To Remote Repo

After the changes have been commited and you want to upload those changes to the remote repo.
1. Run `git push origin <branch>`
	- `<branch>` is the name of the branch you want to push the changes to. You can run `git branch` to find the name of the branch that is currently active.
	- If it is your first time running `git push`, run `git push -u origin <branch>` instead.