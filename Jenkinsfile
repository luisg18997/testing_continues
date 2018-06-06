pipeline{
	agent any
	
	stages{
		stage('build'){
			step{
				fileExists 'User_group.jmx'
			}
		}
		stage('test running'){
			step{
				bzt 'User_group.jmx'
			}
		}
	}
}
