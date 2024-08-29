pipeline {
    agent any

    tools {nodejs "node"}

    stages {
        stage('Build') {
            steps {
                sh 'npm install'
            }
        }
        stage('Test') {
            steps {
                sh 'npm test'
            }
        }
        stage('Deploy') {
            steps {
 naveed
                echo 'Deploying to AWS ( )....'

                sh 'npm run build'
 main
            }
        }
    }
}