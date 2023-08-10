pipeline {

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
