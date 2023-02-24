pipeline {
	agent any
	
	stages {
	    stage('Checkout') {
	        steps {
			checkout scm			       
		      }}
		      options {
  buildDiscarder logRotator(artifactDaysToKeepStr: '', artifactNumToKeepStr: '', daysToKeepStr: '3', numToKeepStr: '4')
}

		stage('Build') {
	           steps {
			  sh '/home/shreena/Documents/GRRAS/apache-maven-3.8.7/bin/mvn install'
	                 }}
		stage('Deployment'){
		    steps {
			
			sh 'cp target/jisho.war /home/shreena/Documents/GRRAS/apache-tomcat-9.0.71/webapps'
	}
}}}
