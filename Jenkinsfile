pipeline {
	agent 
	
	stages[
		stage ('Compile')
			steps{
				withMaven(maven : 'maven3') {
					sh 'mvn clean compile'
				}	
		}
		stage ('Test') 
			steps{
				withMaven(maven : 'maven3'){
					sh 'mvn test'
				}
		}
		stage ('Deployment')
			steps{
				withMaven(maven : 'maven3'){
					sh 'mvn deploy'
				}
		}
	}
}
