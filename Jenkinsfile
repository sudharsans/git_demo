pipeline {
  agent any
  stages {
    stage('Print Message') {
      steps {
        echo 'hello Sudharsan'
      }
    }
    stage('Check Version') {
      steps {
        sh '''packer --version
echo "Checking version"'''
      }
    }
    stage('Done') {
      steps {
        sh 'echo "Done"'
      }
    }
  }
}