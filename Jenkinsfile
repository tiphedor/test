pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
		gcc -Wall -Wextra -Werror main.c -o main
		archiveArtifacts artifacts: 'main', fingerprint: true 
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
		./main
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
		
            }
        }
    }
}
