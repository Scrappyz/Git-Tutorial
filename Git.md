## Before We Start

All `git` commands will be run in the command line eg: `Command Prompt` or `Powershell` on Windows, `Bash` on Linux, etc. 
- If on Windows
	1. Install `Windows Terminal` from the Microsoft Store
	2. Run `Powershell` from the `Windows Terminal`

#### Terminologies

| Word | Definition |
| --- | --- |
| Repo | Short for repository. It is a location where <br> source code and related files are stored <br> and managed in a version control system |
| Local Repo | This is the repository stored in your computer |
| Remote Repo | This is the repository stored in the cloud eg: `Github` |

## Creating Remote Repo

1. Go to `https://github.com/` in the web browser of your choice
	- Sign in or register if you have not
2. Click your profile and go to `Your repositories`
3. Click `New`
4. Fill in the information

## Initialize Local Repo

1. In the command line, go to your project's root directory and run `git init`
2. Go to the repo you created in `https://github.com/` and get the URL of the repo
3. Connect project to remote repo with `git remote add <name> <url>` in the command line

## Commiting Changes

1. To see files that have changes, run `git status`
2. Stage files that you want to commit with `git add <files...>`
	- Use `.` to add all files
3. Commit changes with `git commit -m <message>`

## Pushing Changes To Remote Repo

1. After the changes have been commited, run `git push <name> <branch>`
	- If it is your first time running `git push`, run `git push -u <name> <branch>` instead

## Additional Information

- All `git` commands should be ran in the project's root directory