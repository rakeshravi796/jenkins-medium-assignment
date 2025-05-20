
pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Pulling the image') {
            steps {
               
                // sh 'python3 -m venv venv'
                // sh '. venv/bin/activate'
                sh 'docker pull rakeshravi796/jenkin-python-dock'
            }
        }

        stage('Run file') {
            steps {
                sh 'docker run -p 5000:5000 -t latest rakeshravi796/jenkin-python-dock'
            }
        }

        
    }
}
