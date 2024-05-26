pipeline {
    agent any
    stages {
        stage('Build') { 
            steps {
                mvn clean package
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
