pipeline {
  agent any
  stages {
    stage('dev') {
      steps {
        pwd(tmp: true)
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