
node {
   def mvn = tool name: 'maven', type: 'maven'
   stage('SCM Checkout'){
    // Clone repo
	git 'https://github.com/srikanthweb/my-app-code.git'
   
   }	
   stage('compile package'){
	   // Build using maven
	   
	   sh "${mvn}/bin/mvn package"
   }
	stage('Email Notification'){
	mail bcc: '', body: 'maven build is success full', cc: '', from: '', replyTo: '', subject: 'build package ', to: 'gsri1190@gmail.com'
		
	}
	stage('Slack Notification'){
		slackSend channel: '#udemyproject', color: 'good', message: 'buildsuccess', teamDomain: 'vprofile-projects', tokenCredentialId: 'Slack_Oauth', username: 'srikanth'
	}
	
}

