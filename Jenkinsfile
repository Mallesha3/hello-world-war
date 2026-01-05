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
                dir('hello-world-war') {
                    sh '''
                    pwd
                    ls
                    mvn clean package
                    '''
                }
            }
        }

        stage('Deploy') {
            steps {
                dir('hello-world-war') {
                    sh '''
                    set -e

            echo "WAR files found:"
            ls -l target/*.war

            echo "Deploying WAR"
            scp target/*.war root@3.110.204.120:/opt/tomcat/webapps/

            echo "Restarting Tomcat"
            ssh root@3.110.204.120 "
            /opt/tomcat/bin/shutdown.sh || true
            sleep 5
            /opt/tomcat/bin/startup.sh
            "
                    '''
                }
            }
        }
    }
}

