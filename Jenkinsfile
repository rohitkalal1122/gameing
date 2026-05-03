pipeline {
    agent any

    stages {

        stage('Clone') {
            steps {
                git 'https://github.com/rohitkalal1122/gameing.git'
            }
        }

        stage('Build') {
            steps {
                echo 'Build successful'
            }
        }

        stage('Deploy to XAMPP') {
            steps {
                bat '''
                xcopy /E /I /Y * C:\\xampp\\htdocs\\gameing
                '''
            }
        }
    }
}
