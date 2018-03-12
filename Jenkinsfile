pipeline {
  agent any
  stages {
    stage('DEV') {
      steps {
        sh '''cd /home/ec2-user/DEV
git init
git remote add origin https://github.com/omartinezpou/bbycaSRE
git fetch origin
git checkout -b master --track origin/master
source ~/.bashrc
nvm install stable
ENV=DEV PORT=8084 node bestbuy.ca.js
'''
      }
    }
  }
}