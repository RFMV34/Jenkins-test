pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                bat 'npm install'
                bat 'npm run build'
                archiveArtifacts artifacts: 'dist/**', fingerprint: true
            }
        }
        stage('Test') {
            steps {
                bat 'npm run lint'
                bat 'npm run test-headless'
            }
        }
        stage('Deploy') {
            steps {
               bat 'cp -R dist C:\\Users\\gulanf\\Desktop'
            }
        }
    }
}