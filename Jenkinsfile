pipeline {
agent any
  stages {
  
    stage('Build Image'){
      steps {
      sh '''
         sudo docker build -t node-hello .
         '''
      }
    }

    stage('Deploy Container'){
      steps {
      sh '''
         sudo su
         docker stop node-hello
         docker rm node-hello
         docker run -itd -p 3000:3000 --name node-hello node-hello
         '''
      }
    }
    
    
  }

}
