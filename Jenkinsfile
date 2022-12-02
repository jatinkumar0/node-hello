pipeline {
agent any
  stages {
  
    stage('Build Image'){
      steps {
      sh '''
         docker build -t node-hello .
         '''
      }
    }

    stage('Deploy Container'){
      steps {
      sh '''
         docker stop node-hello
         docker rm node-hello
         docker run -itd -p 3000:3000 node-hello --name node-hello
         '''
      }
    }
    
    
  }

}
