pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        echo 'this is for build'
      }
    }

    stage('test') {
      steps {
        sh '''pwd
ls
echo \'this is for testing\' > sample.txt'''
      }
    }

    stage('deploy in test') {
      parallel {
        stage('deploy in test') {
          steps {
            sleep 10
            echo 'deploy in QA enviroment'
          }
        }

        stage('parallel') {
          steps {
            echo 'parallel practice'
          }
        }

      }
    }

    stage('deploy in prod.') {
      steps {
        sh 'echo \'deploy the code in producton eviroment\''
      }
    }

  }
}