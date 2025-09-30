pipeline {
    agent any

    stages {
        stage('Build') {
            agent {
                docker{
                    image 'node:18-alpine'
                    reuseNode true
                }
               
            }
            steps {
                sh '''
                    ls -la
                    node --version
                    npm --version
                    npm ci
                    npm run build
                    ls -la:
                '''
            }
        }
        stage('Test Build'){
            sh '''
            cat /var/jenkins_home/workspace/Project-1/build/index.html
            npm test
            '''
        }
    }
    stage('Test Build'){
            sh '''
            cat /var/jenkins_home/workspace/Project-1/build/index.html
            npm test
            '''
        }
}