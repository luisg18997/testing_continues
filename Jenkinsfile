node{
	checkout scm
	environment {
        	HOME="."
        	CI = 'true'
   	} 
	dir('jmeter/') {
		parallel TEST VOLUMEN :{
		stage('test running'){
			sh 'pwd'
			bzt 'User_group.jmx'
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
