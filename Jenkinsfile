pipeline {
    agent any
	tools {
        maven 'MAVEN_HOME'
	jdk 'Java'	
    }	
    stages {
	              stage('Load Property file from config server') {
                                   steps {
                                        // load "https://github.com/abhishekmuthyam/config-repo/blob/master/DEV1_PCF.properties"
					 load "C:/Users/muthyama/build/DEV1_PCF.properties"
					   
                                          }
                                }
	    
		stage ('Check out and get property file') {
			steps {
				echo "start call batch script"
				//bat 'https://github.com/abhishekmuthyam/config-repo/blob/master/PCF_CloudService_Script.bat'
				bat 'C:/Users/muthyama/build/PCF_CloudService_Script.bat'
				echo "End call batch script"
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
