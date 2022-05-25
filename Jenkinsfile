pipeline {
  agent {
    docker {
      image 'docker:dind'
      args '--privileged'
    }
  }
  stages {
    stage('Load test on rafaelmarconi.com.br site') {
      steps {
        sh 'docker run -v script.js:/home/k6/script.js loadimpact/k6 run script.js'
      }
    }
  }
}