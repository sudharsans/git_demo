pipeline {
  agent {
    docker {
      image 'maven:3-alpine'
    }

  }
  stages {
    stage('Download Source') {
      steps {
        git 'https://github.com/apache/maven.git'
      }
    }
    stage('Build Maven') {
      steps {
        sh '/usr/local/bin/mvn clean package'
      }
    }
  }
}