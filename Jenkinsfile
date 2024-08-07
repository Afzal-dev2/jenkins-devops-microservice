pipeline {
	agent {
		docker {
			image 'maven:3-alpine'
		}
	}
	stages {
		stage('Build') {
			steps {
				sh 'mvn --version'
				echo 'Building..'
				
			}
		}
		stage('Test') {
			steps {
				echo 'Testing..'
			}
		}
		stage('Deploy') {
			steps {
				echo 'Deploying....'
			}
		}
	}
	 post {
        always {
            echo 'Cleaning up...'
        }
        success {
            echo 'Pipeline succeeded!'
        }
        failure {
            echo 'Pipeline failed!'
		  }  }
}