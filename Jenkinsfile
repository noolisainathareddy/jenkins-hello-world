pipeline {
    agent any
    tools {
        maven 'M313'
    }
    stages {
        stage('Maven clean') {
            steps {
                sh "mvn clean package -DskipTests=true"
            }
        }
        stage('Test') {
            steps {
                sh "mvn test"
            }
        }
    }
}