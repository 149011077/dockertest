pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        sh 'sh \'echo build.\''
      }
    }
    stage('test') {
      steps {
        sh 'sh \'echo test.\''
      }
    }
    stage('deploy') {
      steps {
        sh '''sh \'sleep 130s\'
sh \'echo deploy.\'
'''
      }
    }
  }
}