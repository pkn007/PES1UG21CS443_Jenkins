pipeline {
    agent any
    
    stages {
        stage('Build') {
            steps {
                // Compile the .cpp file using a shell script
                sh 'g++ -o output hello.cpp'
            }
        }
        stage('Test') {
            steps {
                // Print the output of the .cpp file using a shell script
                sh './output'
            }
        }
        stage('Deploy') {
            steps {
                // Add deployment steps here
                // For example, deploy to a server or containerize the application
            }
        }
    }
    
    post {
        always {
            // Display "pipeline failed" in case of any errors
            echo 'Pipeline failed'
        }
    }
}
