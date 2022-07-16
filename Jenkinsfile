pipeline {

  agent {
    docker {
      image "python:2-alpine"
      }
    }

  stages {

    stage("install dependencies ") {
      steps {
        withEnv(["HOME=${env.WORKSPACE}"]) {
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
