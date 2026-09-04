pipeline {
    agent any

    tools {
        maven 'Maven-3.9'
    }

    stages {

        stage('Build') {
            steps {
                sh 'mvn clean compile'
            }
        }

        stage('Test') {
            steps {
                sh 'mvn test'
            }
        }

        stage('Package') {
            steps {
                sh 'mvn package'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deployment stage'
                echo 'Application is ready for deployment'
            }
        }
    }

    post {
        success {
            echo 'Build and Deployment Successful!'
        }

        failure {
            echo 'Build or Deployment Failed!'
        }
    }
}
