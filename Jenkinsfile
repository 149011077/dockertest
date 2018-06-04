pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        sh 'echo "build"'
      }
    }
    stage('test') {
      steps {
        sh 'echo "test"'
      }
    }
    stage('deploy') {
      steps {
        sh '''sleep 130s
echo "deploy"
'''
      }
    }
  }
}