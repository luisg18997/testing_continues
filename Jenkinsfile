pipeline{
	agent any
	
	environment {
        	HOME="."
        	CI = 'true'
   	} 

	stages{
		stage('build'){
			steps{
				fileExists 'User_group.jmx'
			}
		}
		stage('test running'){
			steps{
				bzt 'User_group.jmx'
			}
		}
	}
}
