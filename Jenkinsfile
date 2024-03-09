pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh 'gcc hello.cpp'
        echo 'Build Stage Successful'
      }
    }
    stage('Test') {
      steps {
        sh './a.out'
        echo 'Test Stage Successful'
      }
    }
  }
  post {
    failure {
      echo 'Pipeline failed'
    }
  }
}
