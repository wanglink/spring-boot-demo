pipeline {
  agent any
  stages {
    stage('SIT_CI') {
      parallel {
        stage('SIT_CI') {
          steps {
            sh 'echo "ci"'
          }
        }
        stage('build') {
          steps {
            echo 'build'
          }
        }
      }
    }
    stage('SIT_CD') {
      parallel {
        stage('deploy') {
          steps {
            sh 'echo "sit deploy"'
          }
        }
        stage('sql') {
          steps {
            echo 'sql'
          }
        }
      }
    }
  }
}