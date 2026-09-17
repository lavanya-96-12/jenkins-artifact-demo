pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                git branch: 'main',
                    url: 'https://github.com/lavanya-96-12/jenkins-artifact-demo.git'
            }
        }

        stage('Generate Report') {
            steps {
                bat 'C:\\Users\\lavan\\AppData\\Local\\Programs\\Python\\Python314\\python.exe app.py'
            }
        }

        stage('Archive Report') {
            steps {
                archiveArtifacts artifacts: 'report.txt', fingerprint: true
            }
        }
    }
}
