pipeline {
    agent any

    stages {

        stage('Clone') {
            steps {
                git branch: 'main', url: 'https://github.com/rohitkalal1122/gameing.git'
            }
        }

        stage('Build') {
            steps {
                echo 'Build successful'
                bat 'dir'
            }
        }

        stage('Deploy to XAMPP') {
            steps {
                bat '''
                rmdir /S /Q C:\\xampp\\htdocs\\gameing
                mkdir C:\\xampp\\htdocs\\gameing
                xcopy /E /I /Y * C:\\xampp\\htdocs\\gameing
                '''
            }
        }
    }
}