pipeline {
  agent any
  stages {
    stage('compilar') {
      steps {
        withMaven(maven: 'apache-maven-3.6.3') {
          bat 'mvn clean install -DskipTests=true'
        }

      }
    }

  }
}

