pipeline {
    agent { docker { image 'maven:3.6.2' } }
    stages {
        stage('build') {
            steps {
		sh 'export PATH=/opt/apache-maven-3.6.2/bin:$PATH'
                sh 'mvn --version'
		sh 'cd ~/workspace/Spring/JqueryDemo'
		sh './mvnw clean package'
                sh './mvnw spring-boot:run'
		sh ''	
            }
        }
    }
}
