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
                    sh '''
                    pwd
                    ls
                    cd hello-world-war
                    pwd
                    ls
                    mvn clean package
                '''
            }
        }
    }
}
