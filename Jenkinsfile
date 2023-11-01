pipeline {
	agent{
	label 'Mens-slave'
	}
	stages {
	    stage('Checkout') {
	        steps {
			checkout scm			       
		      }}
		stage('Build') {
	           steps {
			  sh '/home/snehal/Documents/Software/apache-maven-3.9.3/bin/mvn install'
	                 }}
		stage('Deployment'){
		    steps {
			sh 'cp target/netflix.war /home/snehal/Documents/Software/apache-tomcat-9.0.76/webapps'
			}}	
}}
