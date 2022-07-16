pipeline {

  agent any

  stages {

    stage("install dependencies") {
      steps {
        withPythonEnv('python3') {
            sh 'python --version'
          }
        }
      }
  }
}
