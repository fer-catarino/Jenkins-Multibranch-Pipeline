pipeline {
	agent any
		stages {
			stage('First') {
				environment {
					EXECUTE = "True"
				}
				steps {
					sh 'echo "Step One"'
				}
			}
			
			stage('Second') {
				when {
               			 	environment name: 'EXCECUTE', value: 'true'
            			}
				steps {
					 sh 'echo "Updating second stage"'
				}
			}
			
			stage('Third') {
				when {
               			 environment name: 'EXCECUTE', value: 'false'
            			}
				steps {
					script {
						echo "third stage"
					}
				}
			}
		}
}
