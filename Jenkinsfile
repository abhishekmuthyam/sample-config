pipeline {
    agent any
	tools {
       		maven 'MAVEN_HOME'
		jdk 'Java'	
    }	
    stages {
		
		stage('Checkout SCM') {
			steps {
			echo "Start-checkout sample buid"	
	    		git branch: 'masterasdas', credentialsId: 'abhishekmuthyamsadsdd', url: "https://github.com/abhishekmuthyam/sample-build.git"
			echo "End-checkout sample buid"	
			}
			
		}
		
		stage ('Check out and get property file') {
			steps {
				echo "start call batch script"				
				bat 'C:/Users/muthyama/build/PCF_CloudService_Script.bat'
				echo "End call batch script"		
            }			     
        }	
       		 stage('compile') {
				steps {
					load "${WORKSPACE}\\env.properties"
					echo "API_URL: ${API_URL}"
				    	echo "USER_NAME: ${USER_NAME}"
					echo "PASSWORD: ${PASSWORD}"
					echo "ORGANIZATION: ${ORGANIZATION}"
				     	echo "SPACE: ${SPACE}"						      
				}
                        } 
	/*	stage('Package') { 
					steps {
						echo "Build"
						bat "mvn clean compile package -DskipTests"
            }
        } 
		stage('DEPLOY TO PCF') { 
           				 steps {
               					echo "Pivotal Targeted space ${SPACE}"
						bat "cf login -a ${API_URL} -o ${ORGANIZATION} -s ${SPACE} -u ${USER_NAME} -p ${PASSWORD} --skip-ssl-validation"
						bat "cf push sample-config"
            }
        }	*/		
    }
}
