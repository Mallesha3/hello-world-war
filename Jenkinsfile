pipeline {
// agent { label 'Java_Env' }
    agent none

    stages {
        stage('Checkout') {
            agent { label 'Java_Env' }
            steps {
                
                sh 'rm -rf *'
                sh 'git clone https://github.com/Mallesha3/hello-world-war'
            }
        }

       
        }
    }


