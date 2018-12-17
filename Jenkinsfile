pipeline {
  agent any
  stages {
    stage('dev') {
      parallel {
        stage('build1') {
          steps {
            pwd(tmp: true)
          }
        }
        stage('build2') {
          steps {
            sleep 5
            echo 'build2'
          }
        }
        stage('build3') {
          steps {
            echo 'build 3...'
          }
        }
        stage('build4') {
          steps {
            echo 'build4'
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