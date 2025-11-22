pipeline {
    agent any

    tools {
        maven 'Maven 3' // Specify the Maven tool in Jenkins
    }

    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/Ravikiran5105/GitMavenJava.git' 
            }
        }

        stage('Build') {
            steps {
                sh 'mvn clean install' // Build the project
            }
        }

        stage('Test') {
            steps {
                sh 'mvn test' // Run tests (optional)
            }
        }
    }

    post {
        success {
            echo 'Build succeeded!'
        }
        failure {
            echo 'Build failed.'
        }
    }
}
