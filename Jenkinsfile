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
            sh 'date'
          }
        }

        stage('error') {
          steps {
            echo 'Before Deploy the brach will check as well '
          }
        }

      }
    }

    stage('Deploy to test') {
      steps {
        sleep 10
        mail(subject: 'Deployement ', body: 'Hi, This is blue ocean it will come from jenkins', to: 'vipulb.patil580@gmail.com')
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