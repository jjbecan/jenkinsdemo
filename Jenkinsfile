pipeline{
  agent any
  stages{
    stage('Cleanup'){
      steps{
        sh dockercleanup.sh
      }
    }
    stage('Build Docker Image'){
     steps{
        docker build -t flask-app ubtunu/dockerfileexercise/Task1
     }
    }
    stage('Run Container'){
      steps{
        docker run -d -p 80:5500 --name flask-app flask-app
      }
    }
  }
}
