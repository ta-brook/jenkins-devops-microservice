//SCRIPTED

//DECLARATIVE
pipeline {
	agent any
	environment {
		dockerHome = tool 'myDocker'
		mavenHome = tool 'myMaven'
		PATH = "$dockerHome/bin:$mavenHome/bin:$PATH"
	}

	stages {
		stage('Checkout') {
			steps {
				sh "mvn --version"
				echo "Build"
				echo "PATH - $PATH"
				echo "BUILD_NUMBER - $env.BUILD_NUMBER"
				echo "BUILD_ID - $env.BUILD_ID"
				echo "BUILD_URL - $env.BUILD_URL"
			}
		}
		
		stage('Compile') {
			steps {
				sh "mvn clean compile"
			}
		}
		
		stage('Test') {
			steps {
				sh "Test"
			}
		}
		stage('Integration Test') {
			steps {
				sh "mvn failsafe: integration-test failsafe:verify"
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
