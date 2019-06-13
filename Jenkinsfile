node{
	stage('checkout'){
		git credentialsId: 'e11b3922-015f-4548-891b-81fa1bb4a1e5', url: 'https://github.com/vardhan111/jpetstore-6.git'
	}
	stage('mvn package'){
	def mvnHome = tool name: 'maven3', type: 'maven' 
	def mvnCMD = "${mvnHome}/bin/mvn"
	sh label: '', script: "$mvnCMD clean package"
	}
}
