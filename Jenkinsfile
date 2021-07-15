pipeline {
	agent any
		stages {
			stage('First') {
				environment {
					EXECUTE = 'True'
				}
				steps {
					sh 'echo "Step One"'
				}
			}
			
			stage('Second') {
				when {
					EXECUTE = 'True'
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
