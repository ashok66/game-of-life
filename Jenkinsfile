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
        emailext(subject: 'GOL-AutoTest-Report | Jenkins', body: 'Test report', attachLog: true, compressLog: true, from: 'ashok@skillogic.com', replyTo: 'ashok@skillogic.com', to: 'ashok66@gmail.com')
      }
    }
  }
}