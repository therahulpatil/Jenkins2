node('built-in') 
{
    stage('Continuous Download') 
	{
    	git 'https://github.com/therahulpatil/Jenkins2.git'
	}

    stage('Continuous Build') 
	{
    	sh 'mvn package'
	}
	stage('Continuous Deployment') 
	{
    	
        sh ' scp  /home/ubuntu/.jenkins/workspace/Pipe/webapp/target/webapp.war   ubuntu@172.31.32.199:/var/lib/tomcat9/webapps/qaenv.war'

	}
	stage('Continuous Testing') 
	{
    	
	sh 'echo "Testing Passed"'
	}

    stage('Continuous Delivery') 
	{
    	
sh ' scp  /home/ubuntu/.jenkins/workspace/Pipe/webapp/target/webapp.war   ubuntu@172.31.45.237:/var/lib/tomcat9/webapps/prodenv.war'

	}
}
