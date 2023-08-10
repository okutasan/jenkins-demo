pipeline {
environment {
    dockerimagename = "nginx/nginx:latest"
    dockerImage = ""
  }
  agent any

  stages {

    stage('Deploying App to Kubernetes') {
      steps {
        podTemplate {
    node(POD_LABEL) {
        stage('Run shell') {
            sh 'echo hello world'
        }
    }
}
      }
    }

  }

}
