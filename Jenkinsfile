pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                // Checkout the code from Git
                git url: 'https://github.com/username/repo-name.git', branch: 'master' // Adjust the URL and branch as needed
            }
        }

        stage('Install Dependencies') {
            steps {
                // Install the required Python packages
                sh 'pip3 install numpy pandas scikit-learn'
            }
        }

        stage('Run Python Script') {
            steps {
                // Run the Python script
                sh 'python3 creditrisk.py'
            }
        }
    }
    
    post {
        always {
            // Clean up and archive results
            echo 'Build Finished'
        }
    }
}

