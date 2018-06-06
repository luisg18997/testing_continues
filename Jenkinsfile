pipeline{
	agent any
	
	environment {
        	HOME="."
        	CI = 'true'
   	} 
	stages{
	dir('jmeter/') {
		stage('build'){
			steps{
				fileExists 'user_group.jmx'
			}
		}
		stage('test running'){
			steps{
				bzt 'User_group.jmx'
			}
		}
		stage('testing database'){
			steps{
				bzt 'testing_database.jmx'
			}
		}
		stage('testing recording'){
			steps{
				bzt 'login_recording.jmx'
			}
		}
				
	}
	}

	
}
