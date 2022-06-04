pipeline {
    agent none
     agent {
            docker {
                image 'maven:3-alpine'
            }
        }
    stages {
        stage('Build') {
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