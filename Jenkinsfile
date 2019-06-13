pipeline {
	agent any
	stages {
		stage ('compile'){
			steps {
				withMaven (maven : 'maven3') {
					sh 'mvn clean compile'
					}
				}
			}
		}
	 }
