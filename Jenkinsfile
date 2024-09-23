pipeline {
  agent any

  stages {
    stage('Cloning Git') {
      steps {
        git branch: "main",
            url: 'https://github.com/FKFT/felix-node-webapp.git',
        credentialsId: 'FKFT'
        sh 'cd node-express-hello-world'
      }
    }
    stage('Build Container Image') {
      steps {
        agent{
          dockerfile {
              filename '$workspace/Dockerfile',
              
          
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
