pipeline {
  agent any // This tells Jenkins to allocate a workspace and run the pipeline on any available agent
  
  options {
    retry(2)
    }

  stages {
    //   stage('Build') { // Stage 1: Build
    //       steps {
    //           echo 'Building the project...'
    //           // Insert build steps here
              
    //       }
    //   }
    //   stage('Test') { // Stage 2: Test
    //       steps {
    //           echo 'Testing the project...'
    //           // Insert test steps here
    //       }
    //   }
    //   stage('Deploy') { // Stage 3: Deploy
    //       steps {
    //           echo 'Deploying the project...'
    //           // Insert deployment steps here
    //       }
    //   }
  }
  post {
        failure {
            mail to: 'nhisty.dev@gmail.com',
                 subject: 'Pipeline Failure',
                 body: 'The pipeline has failed.'
        }
    }
}