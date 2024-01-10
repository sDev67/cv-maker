pipeline {
  agent any // This tells Jenkins to allocate a workspace and run the pipeline on any available agent

  stages {
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
    }
  post {
        always {
            echo 'HI 1 - This will always run'
        }
        success {
            echo 'HI 2 - This will run only if successful'
        }
        failure {
            mail bcc: '', 
            body: "pipeline failed", 
            cc: '', 
            charset: 'UTF-8', 
            from: '', 
            mimeType: 'text/html', 
            replyTo: '', 
            subject: "ERROR CI: Project", 
            to: "nhisty.dev@gmail.com";
        }
        unstable {
            echo 'This will run only if the run was marked as unstable'
        }
        changed {
            echo 'This will run only if the state of the Pipeline has changed'
            echo 'For example, if the Pipeline was previously failing but is now successful'
        }
    }
}