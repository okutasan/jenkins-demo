pipeline {
  agent any

  stages {

    stage('Deploy To Kubernetes') {
      steps {
        script {
          kubernetesDeploy(configs: "nginx.yaml", kubeconfigId: "kubernetes")
        }
      }
    }

  }

}
