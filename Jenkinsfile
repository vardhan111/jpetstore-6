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
		stage ('metrics stage') {
			steps {
				withMaven (maven : 'maven3') {
					sh 'mvn -p metrics pmd:pmd'
					}
				}
			}
		}
	}
