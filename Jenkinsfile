pipeline {

  agent any

  stages {

    stage("install dependencies ") {
      steps {
        script {
          sh 'pip install pytest'
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
