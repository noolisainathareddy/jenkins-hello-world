pipeline {
    agent any
    tools {
        maven ''
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