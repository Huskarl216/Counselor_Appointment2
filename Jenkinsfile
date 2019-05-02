pipeline 
{
	agent any
	
	stages 
	{
		
		stage('Build') 
		{
			steps 
			{
				sh 'mvn clean'
				sh 'mvn package'
				sh 'docker build -t image1 .'
				sh 'docker build -t image2 -f mysql.Dockerfile .'
			}
		}

		stage('Test')
		{
			steps 
			{
				sh 'mvn test'
			}
		}
		stage('Start Container') 
		{
			steps 
			{
				sh 'docker-compose up'
			}
		}
	}
}
