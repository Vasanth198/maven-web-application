node {

def mavenHome = tool name: "maven 3.8.5"
		
// Checkout Stage
stage ('CheckoutCode'){
git branch: 'development', credentialsId: '480fb18b-cc3c-4381-9aaf-58f82ca235c6', url: 'https://github.com/Vasanth198/maven-web-application.git'
}
		
//Build stage
stage ('Build'){
sh "$mavenHome/bin/mvn clean package"	
}

	/*
//Generate Sonarqube report
stage('SonarQubeReport'){
sh "$mavenHome/bin/mvn sonar:sonar"
}		

//Upload Artifact into Artifactory repo
stage('UploadArtifactToNexus'){
sh "$mavenHome/bin/mvn deploy"
}

//Deploy app into tomcat server
stage('DeployAppIntoTomcat'){
sshagent(['bbcde0e6-583a-4584-920d-41a20f661c89']) {
sh "scp -o StrictHostKeyChecking=no target/maven-web-application.war ec2-user@3.6.37.218:/opt/apache-tomcat-9.0.59/webapps"
}
}

*/
}//Node closing
		
