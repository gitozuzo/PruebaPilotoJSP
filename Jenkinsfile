pipeline {
  agent any
  stages {
    stage('compilar') {
      steps {
        withMaven(jdk: 'C:\\Program Files\\Java\\jdk1.8.0_112', globalMavenSettingsFilePath: 'C:\\Program Files\\Apache Software Foundation\\apache-maven-3.6.3\\conf', mavenSettingsFilePath: 'C:\\Program Files\\Apache Software Foundation\\apache-maven-3.6.3\\conf') {
          bat 'mvn clean install -Dmaven.test.failure.ignore=true'
        }

      }
    }

  }
}