pipeline{
    agent any
     tools{
        maven 'Maven'
        }
    stages{
        stage("test the code"){
            steps{
                echo "========executing A========"
                sh 'date'
            }
        }
        stage('build'){
            steps{
                echo "build the code"
            }
        }
        stage("deploy in prod"){
            steps{
                echo "deploy thr image in production"
            }
        }
    }
    post{
        always{
            echo "========always========"
        }
        success{
            echo "pipeline executed successfull"
        }
        failure{
            echo "pipeline execution failed"
        }
    }
}
