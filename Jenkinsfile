pipeline {
    agent any
    stages {
        stage('Build') {
        docker {
                    image 'maven:3-alpine'
                }
            steps {
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