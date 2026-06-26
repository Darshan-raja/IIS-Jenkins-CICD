pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git branch: 'main',
                    url: 'https://github.com/Darshan-raja/IIS-Jenkins-CICD.git'
            }
        }

        stage('Deploy to IIS') {
            steps {
                bat '''
                robocopy "%WORKSPACE%\\wwwroot" "C:\\inetpub\\wwwroot" /MIR
                if %ERRORLEVEL% LEQ 7 exit /B 0
                exit /B %ERRORLEVEL%
                '''
            }
        }
    }
}
