pipeline {

  agent {
    docker {
      image 'python:3.5.1'
      }
    }

  stages {

    stage("install dependencies ") {
      steps {
        script {
          sh 'python --version'
          sh 'virtualenv venv --distribute . venv/bin/activate pip install -r requirements.txt'
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
