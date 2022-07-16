pipeline {

  agent any

  stages {

    stage("install dependencies ") {
      withPythonEnv('python3') {
        sh 'pip install pytest'
      }
    }

    stage("test") {
      steps {
        sh 'pytest tests/'
      }
    }

    stage("finalise") {
      steps {
        echo "done..."
      }
      }
  }
}
