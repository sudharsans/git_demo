pipeline {
  agent any
  stages {
    stage('Download Source') {
      steps {
        git 'https://github.com/apache/maven.git'
      }
    }
    stage('Build Maven') {
      steps {
        sh 'mvn clean package'
      }
    }
  }
}