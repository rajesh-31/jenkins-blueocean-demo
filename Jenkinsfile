pipeline {
  agent any
  stages {
    stage('A') {
      post {
        always {
          echo '========always========'
        }

        success {
          echo '========A executed successfully========'
        }

        failure {
          echo '========A execution failed========'
        }

      }
      steps {
        echo '========executing A========'
      }
    }

    stage('B') {
      steps {
        sh 'echo "user_name"'
        sh 'echo "BUILS_ID"'
      }
    }

  }
  parameters {
    string(defaultValue: 'rajesh', description: 'who are you ?', name: 'user_name')
  }
}