pipeline {
	agent any
		environment {
			EXECUTE = 'True'
		}
		stages {
			stage('First') {
				steps {
					sh 'echo "Step One"'
				}
			}
			
			stage('Second') {
				when {
					environment name: 'EXECUTE', value: 'True'
            			}
				steps {
					 sh 'echo "Updating second stage"'
				}
			}
			
			stage('Third') {
				when {
               				environment name: 'EXECUTE', value: 'False'
            			}
				steps {
					script {
						echo "third stage"
					}
				}
			}
		}
}
