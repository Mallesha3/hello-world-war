pipeline {
// agent { label 'Java_Env' }
    agent none

    stages {
        stage('Checkout') {
            steps {
                agent { label 'Java_Env' }
                sh 'rm -rf *'
                sh 'git clone https://github.com/Mallesha3/hello-world-war'
            }
        }

       
        }
    }


