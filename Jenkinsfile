pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh 'g++ -o PES2UG20CS563-1 new.cpp'
      }
    }
    stage('Test') {
      steps {
        sh './PES2UG20CS563-1'
      }
    }
    stage('Deploy') {
      steps {
        sh 'mvn deploy'
        echo 'deployment successful'
      }
    }
  }
  post {
    failure {
      echo 'Pipeline failed'
    }
  }
}
