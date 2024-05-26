pipeline {
    agent any
    stages {
        stage('Build') { 
            steps {
                script {
                "mvn clean test"
                }
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
