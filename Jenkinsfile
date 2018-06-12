pipeline {
	agent any
	environment {
        	HOME="."
        	CI = 'true'
   	} 
	stages{
		stage('build'){
			steps{
				sh 'pwd'
				echo 'build'
			}
		}

		stage('testing Volumen'){
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
