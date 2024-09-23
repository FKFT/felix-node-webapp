pipeline {
  agent any

  stages {
    stage('Cloning Git') {
      steps {
        git url: 'https://github.com/FKFT/felix-node-webapp',
        credentialsId: 'FKFT'
      }
    }
    stage('Build Container Image') {
      steps {
        agent{
          dockerfile {
              filename '$workspace/Dockerfile',
              label 'node'              
          }
        }
      }
    }
    stage('Build') {
       steps {
         sh 'npm install'
       }
    }
    stage('Test') {
      steps {
        sh "npm start"
      }
    }    
  }
}
