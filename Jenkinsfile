pipeline {
    agent any


    stages {
        stage('Clone') {
            steps {
                // Get some code from a GitHub repository
                git 'https://github.com/ninotahrbx/testjenkins.git'

            }

        }

        stage('Test') {
            steps {
                // Get some code from a GitHub repository
                bat "mvn test"

            }

        }

        stage('Package') {
            steps {
                // Get some code from a GitHub repository
                bat "mvn package"

            }

        }

    } post {
                // If Maven was able to run the tests, even if some of the test
                // failed, record the test results and archive the jar file.
                success {
                    //junit '*/target/surefire-reports/TEST-.xml'
                    archiveArtifacts 'target/*.jar'
                }
            }
        }
    
