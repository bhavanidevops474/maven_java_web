pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                script {
                "mvn clean install"
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

