pipeline {
    agent any
    stages {
        stage('Build') { 
            steps {
                mvnw -B -DskipTests clean package 
            }
        }
        
     stage('Test') {
        steps {
                mvnw test
            }
            post {
                always {
                    junit 'target/surefire-reports/*.xml'
                }
            }
        }
    }
}
