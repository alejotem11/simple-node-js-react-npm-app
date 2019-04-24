pipeline {
  agent {
    docker {
      image 'node:6-alpine'
      args '-p 3000:3000'
    }

  }
  stages {
    stage('Build') {
      steps {
        echo 'I am in the building stage'
      }
    }
    stage('Test') {
      parallel {
        stage('Test 1') {
          steps {
            echo 'I am in the Testing 1 stage'
          }
        }
        stage('Test 2') {
          steps {
            echo 'I am in the Testing 2 step'
          }
        }
        stage('Test 3') {
          steps {
            echo 'I am in the Testing 3 stage'
          }
        }
      }
    }
    stage('Deliver') {
      steps {
        echo 'I am done!'
      }
    }
  }
  environment {
    CI = 'true'
  }
}