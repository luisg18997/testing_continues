node{
	environment {
        	HOME="."
        	CI = 'true'
   	} 
	dir('jmeter/') {
		stage('build'){
			fileExists 'user_group.jmx'
		}
		stage('test running'){
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
