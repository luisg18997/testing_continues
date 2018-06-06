pipeline{
	agent any
	
	environment {
        	HOME="."
        	CI = 'true'
   	} 

	stages{
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
	}
}
