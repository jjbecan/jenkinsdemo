pipeline{
  agent any
  stages{
    stage('Build Docker Image'){
     steps{
       sh "cd dockerfileexercise/Task1"
       sh "docker build -t flask-app /var/lib/jenkins/workspace/Lab3/dockerfileexercise/Task1"
     }
    }
    stage('Run Container'){
      steps{
        sh "docker run -d -p 80:5500 --name flask-app flask-app"
      }
    }
  }
}
