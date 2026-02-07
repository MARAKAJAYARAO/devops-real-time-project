pipeline {
    agent any

    stages {
        stage('Checkout Code') {
            steps {
                git branch: 'main',
                    url: 'https://github.com/MARAKAJAYARAO/devops-real-time-project.git'
            }
        }

        stage('Build with Maven') {
            steps {
                sh 'mvn clean package'
            }
        }
    }

    post {
        success {
            echo 'BUILD SUCCESSFUL 🎉'
        }
        failure {
            echo 'BUILD FAILED ❌'
        }
    }
}

