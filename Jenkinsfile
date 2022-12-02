pipeline {
agent any
  stages {
  
    stage('Build Image'){
      steps {
      sh '''
         sudo docker build -t node-hello .
         '''
      }

      post {
      always {
      build job : 'deploy' 
      }
    }  
    
    }
    

    
    
  }

}
