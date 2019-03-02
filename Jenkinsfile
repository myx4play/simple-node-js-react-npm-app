pipeline {
    agent any
    
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
    }
}