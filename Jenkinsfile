pipeline {
    agent any
	tools {
        maven 'MAVEN_HOME'
	jdk 'Java'	
    }	
    stages {	           
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
		stage('Package') { 
					steps {
						echo "${SPACE} Build"
						bat "mvn clean compile package -DskipTests"
            }
        } 
		stage('DEPLOY TO PCF') { 
           				 steps {
               				 echo 'pivotal'
             		 	 // bat "cf login -a api.run.pivotal.io -o myapplications -s dev -u abhishekmuthyam@gmail.com -p Chinna23* --skip-ssl-validation"
				//bat "cf push sample-demo"
            }
        }			
    }
}
