pipeline {
    agent any
    stages {
        stage('Build') { 
            steps {
                script {
                "mvn -Dmaven.test.failure.ignore=true install"
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
                success {
                    junit 'target/surefire-reports/*.xml'
                }
            }
        }
    }
}
