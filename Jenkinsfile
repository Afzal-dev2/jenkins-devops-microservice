pipeline {
    agent any
	environment {
		dockerHome = tool 'myDocker'
		mavenHome = tool 'myMaven'
		PATH = "${dockerHome}/bin:${mavenHome}/bin:${env.PATH}"
	}
    stages {
        stage('Checkout') {
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
		stage ('Compile') {
			steps {
				echo 'Compiling...'
				sh 'mvn clean compile'
			}
		}
        stage('Test') {
            steps {
                echo 'Testing...'
				sh 'mvn test'
            }
        }
		 stage('Integration Test') {
            steps {
                echo 'Integration Testing...'
				sh 'mvn failsafe:integration-test failsafe:verify'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying...'
            }
        }
    }
}

