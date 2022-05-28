pipeline {
    agent {
            docker {
                image 'maven:3-alpine'
            }
    }
        stages {
            stage('Build') {
                steps {
                    sh 'mvn clean'
                }
            }
            stage('Test') {
                steps {
                    sh 'mvn test'
                }
                post {
                    always {
                        junit 'target/surefire-reports/*.xml'
                    }
                }
            }
        }
}