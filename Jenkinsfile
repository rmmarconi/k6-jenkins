pipeline {
  agent {
    docker {
      image 'grafana/k6:latest'
    }
  }
  stages {
    stage('Load test on rafaelmarconi.com.br site') {
      steps {
        sh "k6 run script.js"
      }
    }
  }
}