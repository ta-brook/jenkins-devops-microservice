//SCRIPTED

//DECLARATIVE
pipeline {
	agent any
	// agent { docker { image 'maven:3.6.3' } }
	stages {
		stage('Build') {
			steps {
				echo "Build"
				echo "PATH - $PATH"
				echo "BUILD_NUMBER - $env.BUILD_NUMBER"
				echo "BUILD_ID - $env.BUILD_ID"
				echo "BUILD_URL - $env.BUILD_URL"
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

	post {
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
