pipeline {
  agent any // This tells Jenkins to allocate a workspace and run the pipeline on any available agent
    environment {
        MY_VARIABLE = 'Hello, i am sdev!'
    }

  stages {
    stage('Print') {
            steps {
                echo "${MY_VARIABLE}"
            }
        }
        stage('Test') {
            steps {
                echo 'Testing...'
            }
        }
        stage('Print avec date') {
            steps {
                script {
                    def dateTime = new Date()
                    echo "Current date and time: ${dateTime}"
                }
            }
        }
    }
  post {
        always {
            echo 'HI 1 - This will always run'
        }
        success {
            echo 'HI 2 - your pipeline has succeeded'
        }
        failure {
            echo 'HI 3 - your pipeline has failed'
        }
        unstable {
            echo 'HI 4 - This will run only if the run was marked as unstable'
        }
        changed {
            echo 'HI 4 - This will run only if the state of the Pipeline has changed'
            echo 'HI 4 - For example, if the Pipeline was previously failing but is now successful'
        }
    }
}