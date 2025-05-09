pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Stage 1: Build – Compiling and packaging the code using Maven.'
            }
        }

        stage('Unit and Integration Tests') {
            steps {
                echo 'Stage 2: Running unit and integration tests with JUnit.'
            }
        }

        stage('Send Email Notification - Test Stage') {
            steps {
                emailext subject: "Test Stage Completed",
                         body: "The Unit and Integration Tests stage has completed successfully.",
                         to: "kyletking95@gmail.com"
            }
        }

        stage('Code Analysis') {
            steps {
                echo 'Stage 3: Code Analysis – Checking code quality using SonarQube.'
            }
        }

        stage('Security Scan') {
            steps {
                echo 'Stage 4: Security Scan – Identifying vulnerabilities with Snyk.'
            }
        }

        stage('Send Email Notification - Security Scan') {
            steps {
                emailext subject: "Security Scan Completed",
                         body: "The Security Scan stage has completed successfully.",
                         to: "kyletking95@gmail.com"
            }
        }

        stage('Deploy to Staging') {
            steps {
                echo 'Stage 5: Deploying application to AWS EC2.'
            }
        }

        stage('Integration Tests on Staging') {
            steps {
                echo 'Stage 6: Running tests with Postman.'
            }
        }

        stage('Deploy to Production') {
            steps {
                echo 'Stage 7: Deploying application to AWS EC2.'
            }
        }
    }
}
