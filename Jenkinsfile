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
     stage('desplegar') {
      steps {
        deploy adapters: [tomcat7(credentialsId: '81a8db8c-ca88-4b3f-8f9a-42a24fc5c6e6', path: '', url: 'http://localhost:8082')], contextPath: 'ProyectoPilotoJSP', war: '**/*.war'
  
      }
    }    
  }
}



