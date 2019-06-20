pipeline{
	agent any
		stage('build'){
			step{
				sh 'make'
				archiveArtifacts '**/*.jar'
		}
	}
}

