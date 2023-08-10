pipeline {
  agent any

  stages {

    stage('Checkout Source') {
      steps {
        git 'https://github.com/okutasan/jenkins-demo'
      }
    }

    stage('Deploy To Kubernetes') {
      steps {
        script {
          kubernetesDeploy(configs: "nginx.yaml")
        }
      }
    }

  }

}
