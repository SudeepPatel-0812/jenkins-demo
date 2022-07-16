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

    stage("test") {
      steps {
        script {
          sh 'pytest tests/'
        }
      }
    }

    stage("finalise") {
      steps {
        echo "done..."
      }
    }

  }
}
