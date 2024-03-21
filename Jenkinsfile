// Jenkinsfile

pipeline {
    agent any // Run on any available agent

    stages {
        stage('Checkout') {
            steps {
                // Checkout from version control
                checkout scm
            }
        }
        
        stage('Build') {
            steps {
                // Compiles the HelloWorld.java file
                sh 'javac HelloWorld.java'
            }
        }

        stage('Run') {
            steps {
                // Runs the compiled HelloWorld class
                sh 'java HelloWorld'
            }
        }
    }

    post {
        // Post-build actions go here, such as cleaning up, notifications, etc.
        always {
            echo 'The build is finished!'
        }
    }
}
