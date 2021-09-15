pipeline {
    agent none
    stages {
        stage('Integration-testing') {
            agent{
                docker {
                    image 'postman/newman'
                }
            }
            steps {
                sh 'newman --version'
            }
        }
    }
}
