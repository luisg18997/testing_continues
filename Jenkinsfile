pipeline {
	agent any
	environment {
        	HOME="."
        	CI = 'true'
   	} 
	stages{
		stage('build'){
			steps{
				echo 'build'
			}
		}
		stage('test'){
			parallel{
				dir('jmeter/'){	
					stage('testing Volumen'){
						steps{
							sh 'pwd'
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
				
	}
	
}
