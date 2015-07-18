==Ideal==
Every published figure, table, statistical statement is linked to the code and raw data that
generated them.

==Proctice==
To get as close to the ideal as possible.

==Repository on GitHub==
1) For code that you want the public to use and/or improve.
2) For code that used in your manuscripts that have been accepted for publication.
3) For (half-baked) code in an open collaboration that you don't mind the public to see.

==How to==
:: Terminologies
"repo" -- repository
"local" -- the computer you are developing, testing, and running the code
"remote" -- anywhere but "local", usually referring to a repo sitting on GitHub or a Git server
<something> -- non-verbatum description that needs to be replaced by a string 

:: Create a GitHub repository (repo) from an existing project
-1) Install git (https://git-scm.com) on your local machine and learn to use it for revision 
control. [Mac OSX Developer Tools include git.]
0) Sign up for a GitHub account (free) and ask Bosco to add you to the usc-tlab organization.
1) Create an empty repo GitHub in the usc-tlab organization. Give it a descriptive name without 
space (e.g. PRL-eye-movements) and an intelligible description. Do not initialize a README.
2) On you local machine, issue the following commands:
cd <my project>
git init
git add .  ## notice the period
git commit -a -m "Initial commit. v0.1. Have all the pieces, tested with Dataset 1"
git remote add origin https://github.com/usc-tlab/<name of the repo created in Step 1>
git remote -v ## just to double check if the remote has been set up correctly
git push -u origin master

:: Keep the GitHub repo up-to-date
1) Work in <my project> as you would normally do.
2) When you are ready to release the next version, issue the following commands:
cd <my project>
git add .  ## to make sure all the new files are tracked and staged
git commit -a -m "v1.0 tested with 3 datasets"
git push -u origin master

:: Use a GitHub (tlab or otherwise) repo in your own project
1) Log in to GitHub as you and find the repo of interest.
2) Fork the repo to your own GitHub, not the usc-tlab organization.
3) Go to your local computer and issue this command:
git clone https://github.com/<your github username>/<name of the forked repo> <new directory name>
4) cd to <new directory name> and start working!
5) Make full use of git on your local machine while you code. You do not need to push every (local) 
commits.
6) Follow "Keep the GitHub repo up-to-date" to keep your fork on GitHub up-to-date.
7) At a point when you think your change to the code should be merged to the parent repo, issue 
a "pull request" from your GitHub account.  The owner of the parent repo will take care of the 
merging and may ask you to resolve any conflicts (because the parent repo may have gone through 
updates while you are working on the fork).

