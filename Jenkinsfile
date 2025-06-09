pipeline {
    agent any

    tools {
        maven 'Maven 3.8.1' // Ensure this tool is configured in Jenkins
        jdk 'JDK 11'         // Ensure this is installed and named correctly
    }

    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/<your-username>/maven-jenkins-example.git'
            }
        }

        stage('Build') {
            steps {
                sh 'mvn clean compile'
            }
        }

        stage('Run') {
            steps {
                sh 'mvn exec:java'
            }
        }
    }
}
