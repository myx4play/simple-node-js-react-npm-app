pipeline {
    agent any
    
    environment {
        CI = 'true'
    }


    tools {
      nodejs 'node6.11.2'
    }
    
    stages {
        stage('Build') { 
           
            steps {
                // git 'https://github.com/myx4play/simple-node-js-react-npm-app'
                sh 'npm install' 
            }
        }

        stage('Test') {
            steps {
                sh './jenkins/scripts/test.sh'
            }
        }

        stage('Deliver') {
            steps {
                sh './jenkins/scripts/deliver.sh'
                input message: 'Finished using the web site? (Click "Proceed" to continue)'
                sh './jenkins/scripts/kill.sh'
            }
        }
    }
}