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
        stage('Deploy') {
            steps {
                    sh '''
                    ls -l target/*.war

                    scp target/*.war root@3.110.204.120:/opt/tomcat/webapps/

                    ssh root@3.110.204.120 "systemctl restart tomcat"
                '''
            }
        }
    }
}
