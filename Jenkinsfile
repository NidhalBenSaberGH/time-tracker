node {
   def mvn = tool (name: 'Maven', type: 'maven') + '/bin/mvn'
   stage('SCM Checkout'){
    // Clone Git repo
	git branch: 'master', 
	credentialsId: 'github', 
	url: 'https://github.com/NidhalBenSaberGH/time-tracker'
   
   }
   
   stage('Mvn Package'){
	   // Build using maven
	   bat "${mvn} clean package"
   }
}
