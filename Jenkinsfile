pipeline {
  agent any
  stages {
    stage('AWS Setup') {
      steps {
        pwd(tmp: true)
      }
    }
    stage('Prepare to Publish') {
      parallel {
        stage('Prepare to Publish') {
          steps {
            sh 'echo "stage QA"'
          }
        }
        stage('mcu') {
          steps {
            echo 'p1'
          }
        }
        stage('thread') {
          steps {
            echo 'p2'
          }
        }
        stage('bgx') {
          steps {
            echo 'p3'
          }
        }
        stage('') {
          steps {
            echo 'p4'
          }
        }
        stage('') {
          steps {
            echo 'p5'
          }
        }
      }
    }
    stage('Publish') {
      steps {
        sh 'echo "stage prod"'
      }
    }
    stage('AWS Teardown') {
      steps {
        sleep 1
      }
    }
    stage('Notifications') {
      steps {
        echo 'done'
      }
    }
  }
}