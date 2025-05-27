pipeline {
    agent any

    triggers {
        pollSCM('* * * * *') // Optional backup if webhook fails
    }

    stages {
        stage('Checkout') {
            steps {
                git branch: 'experiment',
                    url: 'https://github.com/your-username/project-alpha.git'
            }
        }

        stage('Build') {
            steps {
                echo 'Building the project...'
                // Add build commands here (e.g., make, npm, etc.)
            }
        }

        stage('Test') {
            steps {
                echo 'Running tests...'
                sh 'python3 test.py'  // Assumes test.py is meant to run
            }
        }
    }
}
