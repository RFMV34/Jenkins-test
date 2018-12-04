pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
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
                bat "rm -rf $DIST_PATH"
                bat "cp -R dist\\Jenkins-Test $DIST_PATH"
            }
        }
    }
}