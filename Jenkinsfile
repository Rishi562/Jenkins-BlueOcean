pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh '''pwd
date'''
      }
    }

    stage('test') {
      parallel {
        stage('test') {
          steps {
            echo 'testing'
          }
        }

        stage('parallel test') {
          steps {
            echo 'test parallel'
          }
        }

      }
    }

    stage('deploy') {
      steps {
        echo 'deploy'
        sh 'sleep 10'
      }
    }

  }
}