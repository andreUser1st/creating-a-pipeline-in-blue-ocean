pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh 'npm install'
      }
    }

    stage('uTester Scan') {
      steps {
        utesterstartscan()
      }
    }

  }
}