pipeline {
	agent any
	environment {
        	HOME="."
        	CI = 'true'
   	} 
	stages{
		stage('checkout'){
			steps{
				checkout scm
				echo 'build'
			}
		}
		stage('test'){
			parallel{
				stage('testing Volumen'){
					steps{
						dir('jmeter/'){	
							sh 'pwd'
							bzt 'jmeter/User_group.jmx'
						}
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
