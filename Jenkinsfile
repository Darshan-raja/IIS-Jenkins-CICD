pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Deploy to IIS') {
            steps {
                bat 'robocopy "%WORKSPACE%\\wwwroot" "C:\\inetpub\\wwwroot" /MIR'
            }
        }
    }
}