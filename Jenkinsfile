pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                docker image 'maven:3-alpine'
                sh 'echo "Hello World"'
                sh '''
                    echo "Multiline shell steps works too"
                    ls -lah
                '''
                sh 'mvn --version'
            }
        }
    }
}