
node {
   
   stage('SCM Checkout'){
    // Clone repo
	git 'https://github.com/srikanthweb/my-app-code.git'
   
   }	
   stage('compile package'){
	   // Build using maven
	   
	   sh 'mvn package'
   }
}

