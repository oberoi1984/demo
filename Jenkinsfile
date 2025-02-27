pipeline {
    agent docker-agent-jenkins

    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/oberoi1984/demo.git'
            }
        }

        stage('Build') {
            steps {
                sh 'echo "Building the New Project..."'
                // Add your build commands here (e.g., mvn package, npm install, etc.)
            }
        }

        stage('Test') {
            steps {
                sh 'echo "Running tests..."'
                // Add your test commands here (e.g., pytest, junit, etc.)
            }
        }

        stage('Deploy') {
            steps {
                sh 'echo "Deploying application..."'
                // Add deployment steps (e.g., SCP, Kubernetes, AWS, etc.)
            }
        }
    }

    post {
        success {
            echo 'Pipeline completed successfully!'
        }
        failure {
            echo 'Pipeline failed!'
        }
    }
}
