pipeline {
	agent any
	environment {
		appversion = '1.4'
		SERVER_CREDENTIALS = credentials('dummy_id')
	}
	stages {
		stage("init") {
			steps {
				script {
					echo 'Inside Initialize Step'
				}
			}
		}
		stage("build") {
			when {
				expression {
					appversion == '1.4'
				}
			}
			steps {
				script {
					echo 'Condition is true. Inside Build Step'
					// echo "Building version ${appversion} "
				}
			}
		}
		stage("test") {
			when {
				expression {
					appversion == '2'
				}
			}
			steps {
				script {
					echo 'Inside Test Step'
				}
			}
		}
		stage("deploy") {
			steps {
				script {
					echo 'Inside Test Step'
					echo "deploying using credentials ${SERVER_CREDENTIALS}"
				}
			}
		}
	}
	post {
		always {
			echo 'Inside always'
		}
		failure {
			echo 'inside failure'
		}
		success {
			echo 'sucess'
		}
	}
}
