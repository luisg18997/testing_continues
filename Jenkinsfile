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
			}
		}
		stage('test'){
			parallel{
				stage('testing Volumen'){
					agent {
						label "volumen"
					}
					steps{
						dir('jmeter/'){	
							sh 'pwd'
							bzt 'jmeter/User_group.jmx'
						}
					}
				}
				stage('testing database'){
					agent {
						label "database"
					}
					steps{
						bzt 'testing_database.jmx'
					}
				}
				stage('testing recording'){
					agent {
						label "recording"
					}
					steps{
						bzt 'login_recording.jmx'
					}
				}
			}
		}	
				
	}
	
}
