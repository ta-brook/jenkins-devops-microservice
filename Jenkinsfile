//SCRIPTED

//DECLARATIVE
pipeline {
	agent any
	stages {
		stage('Build') {
			steps {
				echo "Build"
			}
		}
		stage('Test') {
			steps {
				echo "Test"
			}
		}
		stage('Integration Test') {
			steps {
				echo "Integration Test"
			}
		}
	}
	
	pose {
		always {
			echo 'alway run me'
		}
		success {
			echo 'successful'
		}
		failure {
			echo 'failed'
		}
	}
}
