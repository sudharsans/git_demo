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
        sh '/usr/local/bin/mvn clean package'
      }
    }
    stage('Code coverage') {
      steps {
        sh '''/usr/local/bin/mvn sonar:sonar \\
  -Dsonar.host.url=http://localhost:9000 \\
  -Dsonar.login=b502eade536e15bbf0ca2db7abc7ee4ca3573fda'''
      }
    }
  }
}