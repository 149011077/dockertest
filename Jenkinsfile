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
        script {
          def label = "mypod-${UUID.randomUUID().toString()}"
          podTemplate(label: label, cloud: 'kubernetes') {
            node(label) {
              checkout scm
              stage('Run shell') {
                sh 'sleep 30s'
                sh 'echo hello world.'
                sh 'ls'
                sh 'pwd'
              }
            }
          }
        }
        
      }
    }
  }
}