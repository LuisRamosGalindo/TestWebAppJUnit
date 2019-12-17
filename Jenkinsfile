pipeline {
    agent { docker { image 'maven:3.6.2' } }
    stages {
	    
         stage('build') {
            steps {		              
		   sh 'mvn clear'    
		   sh 'mvn compile'    
		   sh 'mvn package'    
                   }
		}
	    
	 stage('Image') {
	     steps{		
		   sh 'mkdir -p target/dependency && (cd target/dependency; jar -xf ../*.jar)'  
		   sh 'docker build -t springio/gs-spring-boot-docker'
		  }
	    	}	
	    
        }    
}
