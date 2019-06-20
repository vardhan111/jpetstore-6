pipeline {
	agent any
	tools {
        maven 'Maven3'
        jdk 'jdk8'
    }
	stages {
		stage('Build'){
			steps {
				sh 'mvn -Dmaven.test.failure.ignore=true install'
			}
			post {
				success {
					junit 'target/surefire-reports/**/*.xml'
				}
			}
		}
	}
}
