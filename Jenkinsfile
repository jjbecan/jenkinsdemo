pipeline{
  agent any
  stages{
    stage('Cleanup'){
      steps{
        sh "sh /home/ubuntu/dockercleanup.sh"
      }
    }
    stage('Build Docker Image'){
     steps{
        sh "docker build -t flask-app -f /dockerfileexercise/Task1/Dockerfile"
     }
    }
    stage('Run Container'){
      steps{
        sh "docker run -d -p 80:5500 --name flask-app flask-app"
      }
    }
  }
}
