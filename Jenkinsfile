pipeline {

  agent any

  stages {

    stage("install dependencies ") {
      steps {
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
