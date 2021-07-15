pipeline {
	agent any
		stages {
			stage('First') {
				steps{
					script {
						env.EXECUTE="true"
					}
				}
			}
			
			stage('Second') {
				when {
               			 	environment name: 'EXCECUTE', value: 'true'
            			}
				steps {
					script {
						echo "Updating second stage"
					}
				}
				
			}
			
			stage('Third') {
				when {
               			 environment name: 'EXCECUTE', value: 'false'
            			}
				steps {
					script {
					}
				}
			}
		}
}
