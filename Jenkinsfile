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
        script {
          def label = "mypod-${UUID.randomUUID().toString()}"
          podTemplate(label: label, cloud: 'kubernetes') {
            node(label) {
              stage('Run shell') {
                sh 'sleep 130s'
                sh 'echo hello world.'
              }
            }
          }
        }
        
      }
    }
  }
}