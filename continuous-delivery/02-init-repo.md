Now that you have a Git repository for the Inventory service, you should push the 
source code into this Git repository.

Go the `inventory-wildfly-swarm` folder, initialize it as a Git working copy and add 
the GitHub repository as the remote repository for your working copy. Make sure you 
replace `GIT-REPO` with the Git repository url in the following commands:

> Paste the Git repository url from the clipboard which you have copied in the 
> previous steps. 

`cd inventory-wildfly-swarm`{{execute}}
`git init`{{execute}}
`git remote add origin GIT-REPO-URL`

Commit and push the existing code to the GitHub repository.

`git add . --all`{{execute}}
`git commit -m "initial add"`{{execute}}
`git push -u origin master`{{execute}}

Enter your Git repository credentials if you get asked to enter your credentials. 
* Username: `developer`
* Password: `developer`

Go to your `inventory-wildfly-swarm` repository web interface and refresh the page. You should 
see the project files in the repository.

![Inventory Repository](https://raw.githubusercontent.com/openshift-roadshow/cloud-native-katacoda/master/assets/cd-gogs-inventory-repo.png)