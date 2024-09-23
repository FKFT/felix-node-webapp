pipeline {
  agent any
  tools {nodejs "node" }
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
              cat '$workspace/Dockerfile'              
          }
        }
      }
    }
    {
    {

       }
    }
{
      {

      }
    }    
  }
}
