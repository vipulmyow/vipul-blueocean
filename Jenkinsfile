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
            echo 'this is test run case '
            sh 'pwd'
            sh '''date
'''
          }
        }

        stage('Test par') {
          steps {
            echo 'Before Deploy the brach will check as well '
          }
        }

      }
    }

    stage('Deploy to test') {
      steps {
        echo 'Test success'
      }
    }

    stage('Deploy to Prod ') {
      steps {
        sh 'date'
        echo 'Successfully run the Pipeline '
      }
    }

  }
}