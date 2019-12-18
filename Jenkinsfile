pipeline {
    agent { docker { image 'maven:3.6.2' } }
    stages {
	    
         stage('build') {
            steps {		
		   sh 'export PATH=/opt/apache-maven-3.6.2/bin:$PATH' 
		   sh 'mvn clear'    
		   sh 'mvn compile'    
		   sh 'mvn package'    
                   }
		}
	    
	 stage('Image') {
	     steps{		
		   sh ''
		  }
	    	}	
	    
        }    
}
