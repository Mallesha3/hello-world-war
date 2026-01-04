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
                    sh '''
                    cd /var/lib/jenkins/workspace/Helloworld_pipeline/hello-world-war
                    '''
                    sh 'pwd'
                    sh 'mvn clean package'
            }
        }
    }
}
