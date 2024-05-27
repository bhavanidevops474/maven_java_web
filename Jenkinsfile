pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                script {
                "mvn -Dmaven.test.failure.ignore=true install"
                }
            }
        
            post {
                success {
                    junit 'target/surefire-reports/*.xml'
                }
            }
        }
        }
    }

