pipeline {
    agent {
            docker {
                image 'maven:3-alpine'
                args '-v /Users/ericzheng/.m2:/Users/ericzheng/.m2'
            }
    }
        stages {
            stage('Build') {
                steps {
                    sh 'mvn -B -DskipTests clean package'
                }
            }
        }
}