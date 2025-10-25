pipeline {
    agent any

    stages {
        stage('Checkout code') {
            steps {
                git branch: 'main', url: 'https://github.com/CecoIvanow/SEDO-Exam-Prep-2-2.git'
            }
        }

        stage('Restore') {
            steps {
                bat 'dotnet restore'
            }
        }
        stage('Install dependencies') {
            steps {
                bat 'dotnet build'
            }
        }
        stage('Test') {
            steps {
                bat 'dotnet test'
            }
        }
    }
}

// test