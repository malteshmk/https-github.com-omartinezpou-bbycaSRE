pipeline {
  agent any
  stages {
    stage('DEV') {
      steps {
        sh '''echo "Deploying on DEV"
cd /home/ec2-user/DEV
rm -rf *
git clone https://github.com/omartinezpou/bbycaSRE
cd bbycaSRE
source ~/.bashrc
nvm install stable
npm install express
npm install ejs
ENV=DEV PORT=8084 node  bestbuy.ca.js &
'''
      }
    }
    stage('TEST') {
      steps {
        sh 'echo "Deploying on TEST"'
      }
    }
    stage('DR') {
      steps {
        sh 'echo "Deploying on DR"'
      }
    }
    stage('PROD') {
      steps {
        sh 'echo "Deploying on PROD"'
      }
    }
  }
}