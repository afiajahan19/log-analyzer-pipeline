pipeline {
    agent any

    stages {
        stage('Run Python Script') {
            steps {
                bat '"C:\\Users\\Afia Jahan\\AppData\\Local\\Programs\\Python\\Python313\\python.exe" analyzer.py'
                bat 'type report.txt'
            }
        }

        stage('Archive Report') {
            steps {
                archiveArtifacts artifacts: 'report.txt', fingerprint: true
            }
        }
    }
}
