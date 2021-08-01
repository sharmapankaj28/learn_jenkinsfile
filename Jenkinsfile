pipeline {
	agent any
	stages {
		stage("init") {
			steps {
				script {
					echo 'Inside Initialize Step'
				}
			}
		}
		stage("build") {
			steps {
				script {
					echo 'Inside Build Step'
				}
			}
		}
		stage("test") {
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
