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
			when {
				expression {
					if BRANCH_NAME == 'main'
				}
			}
			steps {
				script {
					echo 'Condition is true. Inside Build Step'
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
