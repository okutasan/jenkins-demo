node {
  stage('Checkout Source') {
      steps {
        git 'https://github.com/okutasan/jenkins-demo'
      }
    }
  stage('Apply Kubernetes files') {
    withKubeConfig([credentialsId: 'kubernetes', serverUrl: 'https://oktaresear-oktaresearch-2433c1-eushg56k.hcp.southeastasia.azmk8s.io']) {
      sh 'kubectl apply -k redis/kustomization.yaml'
    }
  }
}
