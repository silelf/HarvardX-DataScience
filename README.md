# HarvardX-DataScience
Files for testing course 
Textbook link

This video corresponds to the textbook section on Overview of Git.

Resources link

Explore the repository discussed in the video.

Key points

Recap: there are four stages: working directory, staging area, local repository, and upstream repository
Clone an existing upstream repository (copy repo url from clone button, and type "git clone <url>"), and all three local stages are the same as upstream remote.
The working directory is the same as the working directory in Rstudio. When we edit files we only change the files in this place.
git status: tells how the files in the working directory are related to the files in other stages
edits in the staging area are not tracked by the version control system by default - we add a file to the staging area by git add command
git commit: to commit files from the staging area to local repository, we need to add a message stating what we are doing by git commit -m "something"
git log: keeps track of all the changes we have made to the local repository
git push: allows moving from the local repository to upstream repository, only if you have the permission (e.g. if it is yours)
git fetch: update local repository to  be like the upstream repository, from upstream to local
git merge: make the updated local sync with the working directory and staging area
To change everything in one shot (from upstream to working dir), use git pull (equivalent to combining git fetch + git merge)
Code

pwd
mkdir git-example
cd git-example
git clone https://github.com/rairizarry/murders.git
cd murders
ls
git status
echo "test" >> new-file.txt
echo "temporary" >> tmp.txt
git add new-file.txt
git status
git commit -m "adding a new file" 
git status
echo "adding a second line" >> new-file.txt
git commit -m "minor change to new-file" new-file.txt
git status
git add
git log new-file.txt
git push
git fetch
git merge
