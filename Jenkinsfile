pipeline {
	agent any 
	environment {
	PATH = "$PATH:/usr/local/bin"
	}
	stages {
		stage('Build'){
			steps { 
				echo "Building step"
			}
		} 
 		stage('Stage 2'){
                        steps {
                        	echo "Stage 2 step"
				sh ''' whoami '''
				sh ''' docker info '''
				sh ''' docker-compose -f mongo.yml up '''
       			}
                }

	}	
}	
