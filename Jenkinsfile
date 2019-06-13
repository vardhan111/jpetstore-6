node {
	
	stages{
		stage ('compile') {
			steps{
				withMaven(maven : 'maven3') {
					sh 'mvn clean compile'
				}
			}
		}
		stage ('test') {
			steps{
				withMaven(maven : 'maven3') {
					sh 'mvn test'
				}
			}
		}
	}
}
