pipeline
{
  agent any
  tools
	{
		maven 'Maven-3.6.3'
	}
  stages
  {
   stage('checkout scm')
   {
     steps
	 {
	   git branch: 'master',
       credentialsId: '9baee433-5c76-4599-9c74-51d63d5b804b',
       url: 'https://github.com/vismadhu/Test_repository.git'
	 }
	}
	stage('maven build')
	{
	  steps
	  {
	    script
		 {
		  sh ''' mvn clean package install '''
		 }
	  }
	}
  }
}
