pipeline {
    agent any
    tools {
        maven 'M313'
    }
    stages {
        stage('Maven clean') {
            steps {
                sh "mvn clean package -DskipTests=true"
                sh """
                    echo SLEEP_TIME: ${params.SLEEP_TIME} BRANCH: ${params.BRANCH_NAME}
                """
            }
        }
        stage('Test') {
            steps {
                sh "mvn test"
            }
        }
        stage('Local Deployment') {
            steps {
                sh """ echo "Done with loacal deployement" """
            }
        }
        stage('Integration Testing'){
            steps {
                sh """
                    echo "Done Integration Testing"
                """
            }
        }

    }
}