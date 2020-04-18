pipeline {
	agent any 
	
	stages {
		stage ('GIT') {
			steps{
			 git 'https://github.com/karthikks16/myapp.git'
			}
		}
		stage ('Build') {
			steps{
			sh label: '', script: 'mvn clean'
			sh label: '', script: 'mvn install'
			}
		}
			stage ('Deployment') {
			steps{
		    sh label: '', script: 'cp -rp "/var/lib/jenkins/workspace/Pipeline_proj/target/my-app.war" "/opt/apache-tomcat/webapps"'
			}
		}
	}
}
