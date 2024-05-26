pipeline {
    agent any
    stages {
        stage('Build') { 
            steps {
                script {
                "mvn -B -DskipTests clean package"
                }
            }
        }
        
     stage('Test') {
        steps {
            script {
                "mvn test"
            }
        }
            post {
                always {
                    junit 'target/surefire-reports/*.xml'
                }
            }
        }
    }
}
