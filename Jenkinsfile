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
				sh 'docker build -t huskarl216/basicjava1:image1 .'
				sh 'sudo docker build -t huskarl216/basicjava1:image2 -f mysql.Dockerfile .'
			}
		}

		stage('Test')
		{
			steps 
			{
				sh 'mvn test'
			}
		}

		stage('Deploy') 
		{
		    steps 
		    {
		    	
			}
		}

	}

	post 
	{ 
		always 
		{ 
			sh 'echo "Pipeline Finished"'
		}

		success
		{	
			
		}	
 	}
}