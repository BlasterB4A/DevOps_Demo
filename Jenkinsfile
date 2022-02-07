pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                checkout([$class: 'GitSCM', branches: [[name: '*/master']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/BlasterB4A/DevOps_Demo.git']]])
            }
        }
        stage('Build'){
            steps{
                git 'https://github.com/BlasterB4A/DevOps_Demo.git'
                bat 'python vennevetti.py'
            }
        }
        stage('Test'){
            echo "Test Completed"
        }
    }
}
