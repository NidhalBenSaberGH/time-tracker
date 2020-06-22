node {
   def mvn = tool (name: 'maven3', type: 'maven') + '/bin/mvn'
   stage('SCM Checkout'){
    // Clone Git repo
	git branch: 'master', 
	credentialsId: 'github', 
	url: 'https://github.com/NidhalBenSaberGH/time-tracker'
   
   }
   
   stage('Mvn Package'){
	   // Build using maven
	   
	   sh "${mvn} clean package"
   }
