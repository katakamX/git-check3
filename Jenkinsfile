pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                // Checkout the code from Git
                userRemoteConfigs: [[url: 'https://github.com/katakamX/git-check3.git']]

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

