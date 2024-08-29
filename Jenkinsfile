pipeline {
    agent any

    tools {nodejs "node"}

    stages {
        stage('Build') {
            steps {
                sh 'npm install'
            }
        }
        stage('Scan'){
            steps {
                withSonarQubeEnv(installationName: 'jenkins_sq') {
                    sh 'mvn clean package sonar:sonar'
                }
            }
        }
        stage('Test') {
            steps {
                sh 'npm test'
            }
        }
        stage('Deploy') {
            steps {
                sh 'npm run build'
            }
        }
    }
}