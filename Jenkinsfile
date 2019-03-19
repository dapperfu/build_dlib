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
    stage('Clone dlib') {
      steps {
        git(url: 'https://github.com/davisking/dlib.git', branch: 'master', changelog: true, poll: true)
      }
    }
  }
}