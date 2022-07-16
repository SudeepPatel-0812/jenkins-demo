pipeline {

  agent any

  stages {

    stage("install dependencies ") {
        sh 'pip install pytest'
    }

    stage("test") {
        sh 'pytest tests/'
    }

    stage("finalise") {
        echo "done..."
      }
  }
}
