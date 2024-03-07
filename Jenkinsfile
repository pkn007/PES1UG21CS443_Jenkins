pipeline {
    agent any
    
    stages {
        stage('Build') {
            steps {
                script {
                    // Compile the .cpp file using a shell script
                    sh 'g++ -o hello hello.cpp'
                }
            }
        }
        
        stage('Test') {
            steps {
                script {
                    // Print the output of the .cpp file using a shell script
                    sh './hello'
                }
            }
        }
        
        stage('Deploy') {
            steps {
                // Add deployment steps here if applicable
            }
        }
    }
    
    post {
        always {
            // Display "pipeline failed" in case of any errors
            script {
                currentBuild.result = currentBuild.result ?: 'SUCCESS'
                if (currentBuild.result == 'FAILURE') {
                    echo 'pipeline failed'
                }
            }
        }
    }
}
