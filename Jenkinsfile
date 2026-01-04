pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                sh 'rm -rf *'
               sh 'git clone https://github.com/Mallesha3/hello-world-war'
            }
        }
        stage('Build') {
            steps {
                    sh 'ls'
                    sh 'cd hello-world-war'
                    sh 'ls'
                    sh 'mvn clean package'
            }
        }
    }
}
