pipeline {
environment {
    dockerimagename = "nginx/nginx:latest"
    dockerImage = ""
  }
  agent any

  stages {
       stage('Checkout Source') {
      steps {
        git 'https://github.com/okutasan/jenkins-demo'
      }
    }
    stage('Deploying App to Kubernetes') {
      steps {
        script {
          kubernetesDeploy(configs: "nginx.yaml", kubeconfigId: "kubernetes")
        }
      }
    }

  }

}
