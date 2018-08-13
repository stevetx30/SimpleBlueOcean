pipeline {
  agent any
  stages {
    stage('dev') {
      parallel {
        stage('dev') {
          steps {
            pwd(tmp: true)
          }
        }
        stage('') {
          steps {
            waitForQualityGate true
          }
        }
      }
    }
    stage('qa') {
      steps {
        sh 'echo "stage QA"'
      }
    }
    stage('prod') {
      steps {
        sh 'echo "stage prod"'
      }
    }
  }
}