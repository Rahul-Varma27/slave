pipeline {
	agent{
	label 'slave-node2'
	}
	stages {
	    stage('Checkout') {
	        steps {
			checkout scm			       
		      }}
		stage('Build') {
	           steps {
			  sh '/home/rahul/Files/apache-maven-3.9.6/bin/mvn install'
	                 }}
		stage('Deployment'){
		    steps {
			sh 'cp target/slave.war /home/rahul/Files/apache-tomcat-9.0.85/webapps'
			}}	
}}
