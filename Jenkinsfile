pipeline {
    agent any
    // Final Stages defined here
    stages {
        // Stage 1: Build
        stage('Build') {
            steps {
                echo 'Stage 1: Build - Compiling code into an executable format.'
                echo 'Maven Tool: '
                echo 'An automation tool for Java projects that manages dependencies, compiles code, and runs tests.'
            }
        }
        // Stage 2: Unit and Integration Test
        stage('Test') {
            steps {
                echo 'Stage 2: Test - Conducting unit and integration tests.'
                echo 'Unit Testing - Ensures that individual components work correctly.'
                echo 'Mocha/Chai - A popular dependency used for unit testing in JavaScript/Node.js projects.'
                echo 'Integration Testing: '
                echo 'Testing different aspects of code to ensure they work together as expected.'
                echo 'Postman: '
                echo 'A tool used for API testing, making it useful for integration tests involving RESTful services.'
            }
        }
        // Stage 3: Code Analysis
        stage('Code Analysis') {
            steps {
                echo 'Stage 3: Code Analysis - Improving code quality and reducing risks.'
                echo 'ESLint:'
                echo 'A tool for analyzing JavaScript code for style issues, best practices, and potential bugs.'
            }
        }
        // Stage 4: Security Scan
        stage('Security Scan') {
            steps {
                echo 'Stage 4: Security Scan - Identifying vulnerabilities, weaknesses, and other security risks in codebases.'
                echo 'Veracode: '
                echo 'A scan that analyzes source code for security vulnerabilities without executing the code.'
                echo 'Identifies common security flaws like SQL injection, XSS, and hardcoded secrets.'
            }
        }
        // Stage 5: Deploying
        stage('Deploy to staging') {
            steps {
                echo 'Stage 5: Deploying - Deploying an application to a production or test environment.'
                echo 'AWS EC2 deploy: '
                echo 'A deployment service provided by AWS that automates deploying applications to EC2 instances.'
            }
        }
        // Stage 6: Integration Tests on Staging
        stage('Integration Tests on Staging') {
            steps {
                echo 'Stage 6: Integration Tests on Staging - Verifying that different components or systems work together as expected.'
                echo 'Selenium: For automating browser-based tests, useful for testing web applications.'
            }
        }
        // Stage 7: Deploy to production
        stage('Deploy to production') {
            steps {
                echo 'Stage 7: Deploy to production - Deploying the application to the production server from the staging server.'
                echo 'The same AWS EC2 instance can be used to deploy to the production server.'
            }
            post {
                success {
                    mail to: 'abhimanyurana017@gmail.com',
                    subject: 'Pipeline Success',
                    body: 'Build, Test, Code Analysis, Security Scan, Deploy to Staging, Integration Tests on Staging, and Deploy to Production were successful'
                }
                failure {
                    mail to: 'abhimanyurana017@gmail.com',
                    subject: 'Pipeline Failure',
                    body: 'One or more stages in the pipeline failed'
                }
            }
        }
    }
}
