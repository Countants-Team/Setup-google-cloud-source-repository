# Setup-google-cloud-source-repository


## Setting Up a Repository steps

1. Install Git using following command:
  sudo apt-get install git
2. Install and initialize the Cloud SDK
  cd [repository-name]
3. Enter command - git init 
4. Use the following commands to authenticate
  ```
  gcloud init
  git config credential.helper gcloud.sh
  ```
5. create repository using following command:
  gcloud source repos create [repository-name]
6. Add a repository as a remote:
  git remote add google \https://source.developers.google.com/p/[PROJECT_ID]/r/[CLOUD_SOURCE_REPOSITORY_NAME]
7. Add first deployment using below commands.
```
  git add *
  git commit -m "first deployment"
  git push google master
```
## Cloning a repository steps

1. Install Google Cloud SDK
2. Authenticate using the following command: 
  gcloud init
3. Clone your empty Cloud Repository to a local Git repository: 
  gcloud source repos clone [repository-name] --project=[project name]
4. Switch to your new local Git repository: 
  cd [repository-name] 

Refrenced link - https://cloud.google.com/source-repositories/docs/adding-repositories-as-remotes
