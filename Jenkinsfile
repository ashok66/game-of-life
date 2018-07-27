pipeline {
  agent any
  stages {
    stage('Compile') {
      steps {
        sh 'mvn compile'
      }
    }
    stage('test') {
      steps {
        sh 'mvn test'
        emailext(subject: 'Build results', body: 'Build results', from: 'ashok@skillogic.com', to: 'ashok66@gmail.com', compressLog: true, attachLog: true)
      }
    }
  }
}