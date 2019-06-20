pipeline{
	agent any
	stages{
		stage('build'){
			step{
				sh 'make'
				archiveArtifacts artifacts: "**/target/*.jar',fingerprint:true
			}
		}
	}
}
