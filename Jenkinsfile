pipeline {
    agent any
    
    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }
        stage('Build and Deploy') {
            steps {
                // Create a virtual environment
                bat 'python -m venv venv'
                
                // Activate the virtual environment
                bat 'venv\\Scripts\\activate'
                
                // Install Flask
                bat 'pip install Flask'
                
                // Run the Flask application
                bat 'python app.py &'
            }
        }
    }
}