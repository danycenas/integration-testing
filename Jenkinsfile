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
            environment {
                LC_ALL = 'en_US.UTF-8'
                LANG='en_US.UTF-8'
            }
            steps {
                sh 'newman --version'

                sh 'export LANG=en_US.UTF-8'

                sh 'export LANGUAGE=en_US:en'

                sh 'newman run REST-Petclinic-backend.postman_collection.json'
            }
        }
    }
}
