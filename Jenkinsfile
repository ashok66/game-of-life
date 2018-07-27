pipeline {
  agent any
  stages {
    stage('Compile') {
      steps {
        sh 'mvn compile'
      }
    }
    stage('Test') {
      steps {
        sh 'mvn test'
        emailext(subject: 'Test reports', body: 'Reports', attachLog: true, from: 'ashok@skillogic.com', to: 'ashok66@gmail.com')
      }
    }
  }
}