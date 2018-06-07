node{
	checkout scm
	environment {
        	HOME="."
        	CI = 'true'
   	} 
	dir('jmeter/') {
		stage('test'){
			parallel{
				stage('testing Volumen'){
					sh 'pwd'
					bzt 'jmeter/User_group.jmx'
				}
				stage('testing database'){
					bzt 'testing_database.jmx'
				}
				stage('testing recording'){
					bzt 'login_recording.jmx'
				}
			}
		}	
				
	}
	
}
