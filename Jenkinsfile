pipeline {
  agent any
  stages {
    stage('dev') {
      parallel {
        stage('dev') {
          steps {
            sh '''echo env
'''
          }
        }
        stage('dev_1') {
          steps {
            echo 'hello i am dev 1'
          }
        }
        stage('dev_2') {
          steps {
            sleep 300
          }
        }
      }
    }
    stage('int') {
      parallel {
        stage('int') {
          steps {
            sh 'echo env'
          }
        }
        stage('int_1') {
          steps {
            sh 'env'
          }
        }
        stage('int3') {
          steps {
            sh 'env'
          }
        }
      }
    }
    stage('prod') {
      steps {
        sh 'echo "go prod"'
      }
    }
  }
}