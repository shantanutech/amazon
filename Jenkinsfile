pipeline {
	agent any
	
	stages {
	    stage('Checkout') {
	        steps {
			checkout scm			       
		      }}
		stage('Build') {
	           steps {
			  sh '/home/shantanu/Documents/jenkins/apache-maven-3.8.7-bin/apache-maven-3.8.7/bin/mvn install'
	                 }}
		stage('Deployment'){
		    steps {
			
			sh 'sshpass -p "jenkins" scp target/amazon.war slave@172.17.0.2:/home/slave/server/apache-tomcat-9.0.70/webapps'	}
}}}
