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
        sh 'docker run -v ${WORKSPACE}/tests:/home/k6/ loadimpact/k6 run tests/script.js'
      }
    }
  }
}