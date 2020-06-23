pipeline {
    agent {
        docker {
            image 'maven:3-alpine'
            args '-v $HOME/.m2:/root/.m2'
        }
    }
    	
    stages {
	stage('SCM Checkout'){
	    steps{
	        // Clone Git repo
	        git branch: 'master',
	        url: 'https://github.com/NidhalBenSaberGH/time-tracker'
	    }
	    
        }
	    
        stage('Build') {
            steps {
                 bat 'clean package'
            }
        }
    }
}
