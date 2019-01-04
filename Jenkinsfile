pipeline {
  agent none
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
            node(label: 'myNode1') {
              echo 'hello'
            }

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
        stage('error') {
          steps {
            echo 'p4'
          }
        }
        stage('error') {
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