pipeline {
    agent any
    stages {
        // stage('Clone repository') {
        //     steps {
        //         checkout([$class: 'GitSCM', branches: [[name: '*/main']], userRemoteConfigs: [[url: 'https://github.com/tarunsairaj/PES2UG21CS572_Jenkins']]])
        //     }
        // }
        stage('Build') {
            steps {
                build 'PES2UG21CS572-1'
                sh 'g++ main.cpp -o output'
            }
        }
        stage('Test') {
            steps {
                // Assuming you have test steps here. Adjust accordingly.
                sh './output'
            }
        }
        stage('Deploy') {
            steps {
                echo 'deploy'
                // Assuming you have deployment steps here. Adjust accordingly.
            }
        }
    }
    post {
        failure {
            echo 'Pipeline failed'
            // You can add additional actions to take upon failure here.
        }
    }
}
