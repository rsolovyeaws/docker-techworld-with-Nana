pipeline {
	agent any 
	stages {
		stage('Build'){
			steps { 
				echo "Building step"
			}
		} 
 		stage('Stage 2'){
                        steps {
                        	echo "Stage 2 step"
				sh ''' docker info '''
       			}
                }

	}	
}	
