pipeline{
	agent any
	stages{
		stage('build'){
			step{
				sh 'make'
				archiveArtifacts '**/*.jar'
			}
		}
	}
}
