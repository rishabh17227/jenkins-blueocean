pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh '''pwd
date'''
      }
    }

    stage('Test') {
      parallel {
        stage('Test') {
          steps {
            echo 'test step in process'
          }
        }

        stage('test-parallel') {
          steps {
            echo 'test parallel in process'
          }
        }

      }
    }

    stage('deploy') {
      steps {
        echo 'deploying the code'
        sleep 13
      }
    }

  }
}