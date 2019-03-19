pipeline {
  agent any
  stages {
    stage('DEBUG') {
      parallel {
        stage('pwd') {
          steps {
            sh 'pwd'
          }
        }
        stage('env') {
          steps {
            sh 'env'
          }
        }
      }
    }
  }
}
