pipeline {
        agent any
	stages {
		stage("init") {
			steps {
				script {
					echo 'Initialize step'
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
