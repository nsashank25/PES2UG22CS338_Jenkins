pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                script {
                    sh 'g++ -o PES2UG22CS338 hello.cpp' // Intentional error in the Jenkinsfile
                }
            }
        }

        stage('Test') {
            steps {
                script {
                    sh './PES2UG22CS338'
                }
            }
        }

        stage('Deploy') {
            steps {
                echo 'Application is being Deployed.'
            }
        }
    }

    post {
        failure {
            echo 'Pipeline has failed'
        }
    }
}
