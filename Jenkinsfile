pipeline {
    agent any
	tools {
        maven 'MAVEN_HOME'
	jdk 'Java'	
    }	
    stages {
		stage ('Initialize') {
			steps {
				bat 'C:/Users/muthyama/build/PCF_CloudService_Script.sh'
                		bat 'mvn --version'
				
            }			     
        }
      /*  stage('Package') { 
            steps {
			echo "Dev Build"
			bat "mvn clean compile package -DskipTests"
            }
        } */
    }
}
