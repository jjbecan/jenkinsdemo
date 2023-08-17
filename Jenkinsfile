pipeline{
  agent any
  stages{
    stage('Build Docker Image'){
     steps{
        sh "docker build -t flask-app ."
     }
    }
    stage('Run Container'){
      steps{
        sh "docker run -d -p 80:5500 --name flask-app flask-app"
      }
    }
  }
}
