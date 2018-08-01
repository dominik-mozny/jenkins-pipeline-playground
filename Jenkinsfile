pipeline {
  agent {
    docker {
      image 'maven:3.5.4-jdk-8'
    }

  }
  stages {
    stage('Initialize') {
      steps {
        sh '''echo PATH = ${PATH}
echo M2_HOME = ${M2_HOME}
mvn clean'''
      }
    }
    stage('Build') {
      steps {
        sh 'mvn install -Dmaven.test.failure.ignore=true'
      }
    }
  }
}