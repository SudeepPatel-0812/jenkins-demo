pipeline {

  agent any

  stages {

    stage("install dependencies ") {
      steps {
        script {
          sh 'pip install -r requirements.txt'
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
