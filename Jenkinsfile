pipeline {
	agent any
	//{
		// docker {
		// 	image 'maven:3'
		// }
	}
	stages {
		stage('Build') {
			steps {
				// sh 'mvn --version'
				// echo 'Building..'
				echo "Build"
				echo "PATH = $PATH"
				echo "BUILD_NUMBER = $env.BUILD_NUMBER"
				echo "BUILD_ID = $env.BUILD_ID"
				echo "BUILD_URL = $env.BUILD_URL"
				echo "JOB_NAME = $env.JOB_NAME"


				
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
