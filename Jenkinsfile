pipeline {
environment {
    dockerimagename = "nginx/nginx:latest"
    dockerImage = ""
  }
  agent any

  stages {

    stage('Deploying App to Kubernetes') {
      steps {
        script {
          kubernetesDeploy(configs: "nginx.yaml", kubeconfigId: "kubernetes")
        }
      }
    }

  }

}
