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
        sh 'cat tests/script.js | docker run -i loadimpact/k6 run -'
      }
    }
  }
}