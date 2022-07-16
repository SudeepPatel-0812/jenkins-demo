pipeline {

  agent any

  stages {

    stage("install dependencies ") {
      step {
        sh 'pip install pytest'
      }
    }

    stage("test") {
      step {
        sh 'pytest tests/'
      }
    }

    stage("finalise") {
      step {
        echo "done..."
      }
      }
  }
}
