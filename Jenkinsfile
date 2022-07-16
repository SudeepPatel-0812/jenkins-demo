pipeline {

  agent any

  stages {

    stage("install dependencies") {
      steps {
        withPythonEnv(python: 'python-3.8.0') {
          sh "pip install -r requirements.txt --user"
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
