pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh 'g++ hello.cpp -o output'
        echo 'Build Stage Successful'
      }
    }
    stage('Test') {
      steps {
        sh './output.out'
        echo 'Test Stage Successful'
      }
    }
    stage('Deploy') {
      steps {
        echo 'Deploy Stage Successful'
      }
    }
  }
  post {
    failure {
      echo 'Pipeline failed'
    }
  }
}
