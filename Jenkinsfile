pipeline {
	//agent any
	agent {
		label 'slavevm'
	}
	
	tools {
		maven 'Maven3.8.4'
	}
	/*environment {
		mavenHome = "/var/lib/jenkins/tools/hudson.tasks.Maven_MavenInstallation/Maven3.8.4/"
		//def mavenHome = tool name: "Maven3.8.4"
	}*/
	options {
		buildDiscarder(logRotator(numToKeepStr: '10'))
		timeout(time: 60, unit: 'MINUTES')
	}
	stages {
		/*stage ('Checkoutcode'){
			steps {
				git credentialsId: 'githubuser', url: 'https://github.com/sureshdevops99/mbpdevops.git'
			}
		}*/
		stage ('Build') {
			steps {
				//withMaven(maven: 'Maven3.8.4') {
					//sh "${mavenHome}/bin/mvn clean package"
					sh "mvn clean package"
				//}
			}
		}
	}
}
