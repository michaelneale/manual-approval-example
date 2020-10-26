pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh 'echo building'
            }            
        }
        stage('Deploy') {
            when {
                environment name: "CI_BUILD_APPROVED", value: "true"
            }
            steps {
                sh "echo deploying"
            }
        }
    }
}