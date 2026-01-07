pipeline {
agent any

 parameters {
        string(name: 'CMD', defaultValue: 'cd', description: 'command used to run or to build application')
        booleanParam(name: 'RUN_TESTS', defaultValue: false, description: 'Run tests?')
        choice(name: 'CMD1', choices: ['clean', 'validate', 'compile'], description: 'test package deploy')
    }
 
 //agent { label 'Java_Env' }
  //  agent none

    stages {
        stage('Checkout') {
            //agent { label 'Java_Env' }
            steps {

              sh 'echo welcome'
                //sh 'rm -rf *'
                //sh 'git clone https://github.com/Mallesha3/hello-world-war'
            }
        }
    }
}
