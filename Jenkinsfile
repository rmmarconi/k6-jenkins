pipeline {
  agent {
    docker {
      image 'grafana/k6:latest'
    }
  }
  stages {
    stage('Load test on rafaelmarconi.com.br site') {
      steps {
        sh "run script.js"
      }
    }
  }
}