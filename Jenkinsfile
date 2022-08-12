pipeline {
  agent any
  stages {
    stage('checkout git') {
      steps {
        git(url: 'https://github.com/elestopadov/jenkins-example-app.git', branch: 'main')
      }
    }

    stage('build') {
      steps {
        echo 'this is build'
      }
    }

    stage('deploy') {
      parallel {
        stage('deploy to dev_1') {
          steps {
            sleep 30
            echo 'finished'
          }
        }

        stage('deploy to dev_2') {
          steps {
            sleep 50
            echo 'completed'
          }
        }

      }
    }

    stage('test') {
      steps {
        echo 'test'
      }
    }

  }
  environment {
    home = '/opt/dir'
  }
}