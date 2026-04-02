pipeline {
    agent any

    stages {
        stage('Clone Repo') {
            steps {
                git 'https://github.com/aryan249123-rgb/vivin-midterm.git'
            }
        }

        stage('Verify Files') {
            steps {
                bat 'echo Checking files...'
                bat 'dir'
            }
        }

        stage('Deploy to Local Folder') {
            steps {
                bat 'mkdir C:\\deploy-html'
                bat 'xcopy /E /I /Y * C:\\deploy-html'
            }
        }

        stage('Open in Browser') {
            steps {
                bat 'start C:\\deploy-html\\index.html'
            }
        }
    }
}