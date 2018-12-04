pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo "Say $start"
                bat 'npm install'
                bat 'npm run build'
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
               bat 'cp -R dist\\Jenkins-Test C:\\Users\\gulanf\\Desktop\\JenkinsTest'
            }
        }
    }
}