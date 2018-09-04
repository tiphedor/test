pipeline {
     agent {
	docker { image 'gcc:5' }
     }

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
		sh 'gcc -Wall -Wextra -Werror main.c -o main'
		archiveArtifacts artifacts: 'main', fingerprint: true 
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
		sh './main'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
		
            }
        }
    }
}
