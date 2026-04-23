pipeline {

	agent any 

	triggers {
		cron('H/2 * * * *')
	}

	stages {
		stage('Initialisation') {
			steps {
				echo 'initializing the process'
			}
		}
		
		stage('Pipeline script') {
			parallel { 
				stage('Quality testing') {
					steps {
						echo 'testing the quality'
					}
				}
				stage('Improving user interface') {
					steps {
						echo 'improving the window'
					}
				}
			}
		}
		
		stage('Termination') {
			steps {
				echo 'terminating the process'
			}
		}
	}
	post {
		success { 
			echo 'the test is successful'
		}
	}
}
