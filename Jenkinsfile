pipeline {
	agent any
	stages {
		stage ('compile'){
			step {
				withMaven (maven : 'maven3') {
					sh 'mvn clean compile'
					}
				}
			}
		stage ('metrics stage') {
			step {
				withMaven (maven : 'maven3') {
					sh 'mvn -p metrics pmd:pmd'
					}
				}
			}
		}
	}
}