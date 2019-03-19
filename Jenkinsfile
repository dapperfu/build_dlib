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
    stage('Build dlib') {
      steps {
        sh 'mkdir build; cd build; cmake ../dlib -DUSE_AVX_INSTRUCTIONS=1; cmake --build .'
      }
    }
  }
}