pipeline {
    agent none
    stages {
        stage('Integration-testing') {
            agent{
                docker {
                    image 'postman/newman'
                    args '--entrypoint=""'
                }
            }
            steps {
                sh 'newman --version'
            }
        }
    }
}
