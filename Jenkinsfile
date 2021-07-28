pipeline {
    agent any
    stages {
        stage('Test') {
            steps {
                sh 'make check'
            }
        }
    }
    post {
        always {
            junit '**/target/*.xml'
        }
        failure {
            emailext body: 'hi abdul qadir', subject: 'testing message', to: 'aq2072417@gmail.com'
        }
    }
}
