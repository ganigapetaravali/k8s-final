pipeline {
agent any 
 environment {
   imageName = "kushal"
   registryCredencials = "http://ec2-18-212-25-74.compute-1.amazonaws.com:8081/"
   registry = "http://18.212.25.74:8081/repository/k8s-task/"
   dockerImage = ""
}
 stages {
  stage("checkout Repo") {
   steps {
     git branch: 'main', url: 'https://github.com/ganigapetaravali/task.git'
     }
    }
   }
 stages("Build image") {
  steps {
   script {
     dockerimage = sh 'docker build -t flask:1.0 .'
      }
    }
  }
}
