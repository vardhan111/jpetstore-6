node{
	stage('checkout'){
		git credentialsId: 'e11b3922-015f-4548-891b-81fa1bb4a1e5', url: 'https://github.com/vardhan111/jpetstore-6.git'
	}
	stage('mvn package'){
	def mvnHome = tool name: 'maven3', type: 'maven' 
	def mvnCMD = "${mvnHome}/bin/mvn"
	sh label: '', script: "$mvnCMD clean package"
	}
	stage('deploy'){
	sh label: '', script: '''scp /target/*.war ec2-user@ec2-107-23-92-5.compute-1.amazonaws.com:/opt/tomcat8/apache-tomcat-8.5.42/webapps
'''
	}
}
