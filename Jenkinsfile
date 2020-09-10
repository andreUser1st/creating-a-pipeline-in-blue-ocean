pipeline {
  agent any
  stages {
    stage('Build') {
      parallel {
        stage('Build') {
          steps {
            sh 'npm install'
          }
        }

        stage('uTester Scan - CNN') {
          steps {
            utesterstartscan baseAddress: 'https://www.cnn.com', errorsHigh: '', errorsLow: '', errorsMedium: '', errorsSuggestions: '', project: 'Pre-sales', scanSettingsId: 'c1e0b8dd-65cc-46f7-a52c-fe1dd3620d98'
            sleep 20
          }
        }

      }
    }

    stage('uTester Scan') {
      steps {
        utesterstartscan baseAddress: 'https://www.cnn.com', errorsHigh: '', errorsLow: '', errorsMedium: '50', errorsSuggestions: '', project: 'Pre-sales', scanSettingsId: 'c1e0b8dd-65cc-46f7-a52c-fe1dd3620d98'
        sleep 20
      }
    }

  }
}
