pipeline {
  environment {
   image Name = "kushal"
    registry = "http://ec2-18-212-25-74.compute-1.amazonaws.com:8081/"
    registryCredential = 'nexusrepo'
    dockerImage = ""
    }
  stages {
    stage('CheckoutRepo') {
      steps {
      Checkout   (git branch: 'main', url: 'https://github.com/ganigapetaravali/task.git')
      }
    }
   stage('Building image') {
      steps{
        script {
         dockerImage = 'docker.build.flask .'
        }
       }
	  }
