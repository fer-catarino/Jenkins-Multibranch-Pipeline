pipeline {
	agent any
		stages {
			stage('First') {
				script {
					env.EXECUTE="true"
				}
			}
			stage('Second') {
				script {
					echo ${EXECUTE}
				}
				when {
               			 environment name: 'EXCECUTE', value: 'true'
            			}
			} 
			stage('Third') {
				when {
               			 environment name: 'EXCECUTE', value: 'false'
            			}
			}
		}
}
