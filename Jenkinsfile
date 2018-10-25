pipeline {
  agent any
  stages {
    stage('SIT_CI') {
      parallel {
        stage('dev_checkout') {
          steps {
            echo 'dev_checkout'
          }
        }
        stage('sit_merge') {
          steps {
            sh 'echo "merge dev to sit"'
          }
        }
        stage('build') {
          steps {
            echo 'build'
          }
        }
        stage('package') {
          steps {
            sh 'echo "mvn package"'
          }
        }
      }
    }
    stage('SIT_CD') {
      steps {
        sh 'echo "upgrade"'
      }
    }
  }
}