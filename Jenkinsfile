node('built-in') 
{
    stage('Continuous Download_MASTER') 
	{
    git 'https://github.com/sunildevops77/maven.git'
	}
    stage('Continuous Build_MASTER') 
	{
    sh label: '', script: 'mvn package'
	}
    stage('Continuous Deployment_MASTER') 
	{
sh label: '', script: 'scp /home/ubuntu/.jenkins/workspace/ScriptedPipeline/webapp/target/webapp.war   ubuntu@172.31.83.88:/var/lib/tomcat8/webapps/qaenv.war'
	}
    stage('Continuous Testing_MASTER') 
	{
              sh label: '', script: 'echo "Testing Passed"'
	}
    stage('Continuous Delivery_MASTER') 
	{
sh label: '', script: 'scp /home/ubuntu/.jenkins/workspace/ScriptedPipeline/webapp/target/webapp.war   ubuntu@172.31.82.16:/var/lib/tomcat8/webapps/prodenv.war'
	}
}
