pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        echo 'Hello world ! Jenkins pipeline '
        sh './mvnw clean compile'
      }
    }

    stage('UnitTest') {
      steps {
        sh './mvnw test'
        junit '**/target/surefire-reports/TEST-*.xml'
      }
    }

  }
}