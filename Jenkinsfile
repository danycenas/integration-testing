pipeline {
    agent none
    environment {
        LC_ALL = 'en_US.UTF-8'
        LANG    = 'en_US.UTF-8'
        LANGUAGE = 'en_US.UTF-8'
    }
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

                sh 'newman run REST-Petclinic-backend.postman_collection.json'
            }
        }
    }
}
