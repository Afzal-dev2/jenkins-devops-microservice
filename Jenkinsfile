pipeline {
	agent {
		docker {
			image 'maven:3-alpine'
		}
	}
	stages {
		stage('Build') {
			steps {
				echo 'Building..'
				sh 'mvn --version'
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