pipeline {
  agent any

  stages {
    stage('CODE') {
      steps {
        git url:"", branch:"main"
      }
    }
  }
  stages {
    stage('EKS CLUSTER DEPLOY') {
      steps {
        sh " aws eks --region ap-south-1 update-kubeconfig --name netlicluster "
        sh " kubectl get pods"
      }
    }
  }
}
