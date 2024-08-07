pipeline {
    agent any
	environment {
		dockerHome = tool 'myDocker'
		mavenHome = tool 'myMaven'
		PATH = "${dockerHome}/bin:${mavenHome}/bin:${env.PATH}"
	}
    stages {
        stage('Build') {
            steps {
                echo 'Building...'
				sh 'mvn --version'
				sh 'docker version'
				echo "PATH = $PATH"
				echo "BUILD_NUMBER = $env.BUILD_NUMBER"
				echo "BUILD_ID = $env.BUILD_ID"
				echo "BUILD_URL = $env.BUILD_URL"
				echo "JOB_NAME = $env.JOB_NAME"
            }
        }
        stage('Test') {
            steps {
                echo 'Testing...'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying...'
            }
        }
    }
}

