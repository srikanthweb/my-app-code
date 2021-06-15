
node {
   def mvn = tool (name: 'apache-maven-3.6.3', type: 'maven') + '/opt/apache-maven-3.6.3'
   stage('SCM Checkout'){
    // Clone repo
	git 'https://github.com/srikanthweb/my-app-code.git'
   
   }	
   stage('compile package'){
	   // Build using maven
	   
	   sh "${mvn} package"
   }
}

