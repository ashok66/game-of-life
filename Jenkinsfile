pipeline {
  agent any
  stages {
    stage('Compile') {
      steps {
        build(job: 'compile', quietPeriod: 5)
        sh 'mvn compile'
      }
    }
  }
}