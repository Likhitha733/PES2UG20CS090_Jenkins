pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh 'g++ -o PES2UG20CS090-1 hello.cpp
            }
        }

        stage('Test') {
            steps {
                sh './PES2UG20CS090-1'
            }
        }

        stage('Deploy') {
            steps {
              echo 'Deployment Successful' 
              //sh 'mvn deploy'
                // Add steps to deploy the build artifact
            }
        }
    }

    post {
        always {
            script {
                if (currentBuild.result == 'FAILURE') {
                    echo 'pipeline failed'
                }
            }
        }
    }
}
