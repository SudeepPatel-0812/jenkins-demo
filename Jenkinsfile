pipeline {

  agent {
    docker {
      label "docker && linux"
      image "python:3.7.2"
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
