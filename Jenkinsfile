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
            sleep 5
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