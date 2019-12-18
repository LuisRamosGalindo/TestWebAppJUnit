pipeline {
	
     environment {
          registry = 'rgalindoluis/ibkappweb-docker'
          registryCredential = 'dockerhub'
     }	
	
    agent { docker { image 'maven:3.6.2' } }
    stages {
	    
         stage('build') {
            steps {		
		   sh 'export PATH=/opt/apache-maven-3.6.2/bin:$PATH' 
		   sh 'mvn clean'    
		   sh 'mvn compile'    
		   sh 'mvn package'    
                   }
		}
	    
	 stage('Image') {
	     steps{		
		    script{          		   
			   docker login -u  rgalindoluis  -p  Pelusa1984$ docker.io
			   docker build -t rgalindoluis/ibkappweb-docker:latest .
			   docker push rgalindoluis/ibkappweb-docker:latest   
        	    }
		  }
	    	}	
	    
        }    
}
