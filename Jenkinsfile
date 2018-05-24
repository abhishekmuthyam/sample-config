pipeline {
    agent any
	tools {
        maven 'MAVEN_HOME'
	jdk 'Java'	
    }	
    stages {
		stage ('Initialize') {
			steps {
				echo "start call batch script"
				bat 'C:/Users/muthyama/build/PCF_CloudService_Script.bat'
				echo "End call batch script"
				echo "finally deploy to ${DEPLOY_ENV}_PCF_Properties"
				//echo "start yml"
				//bat 'C:/Users/muthyama/build/DEV1_PCF_Properties.yml'
				//echo "end yml"
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
