pipeline {
    agent {
            docker 'maven:3.3.3'
    }
        stages {
            stage('Build') {
                steps {
                    sh 'mvn --version'
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