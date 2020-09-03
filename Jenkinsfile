pipeline {
    agent none
    stages {
        stage('Install node') {
            agent {
                docker { image 'node:10' }
            }
            steps {
                sh 'node --version'
            }
        }
        stage('Cypress tests') {
            agent {
                docker { image 'cypress/base:10' }
            }
            steps {
                sh 'npx cypress run'
            }
        }
    }
}