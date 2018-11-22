node('master') 
{ 
    stage('ContinuousDownload-test') 
    {
       git 'https://github.com/selenium-saikrishna/maven.git'
    }
    stage('ContinuousBuild-test')
    {
        sh 'mvn package'
    }
    stage('ContinuousDeployment-test')
    {
        sh 'scp /home/ubuntu/.jenkins/workspace/myproject/webapp/target/webapp.war ubuntu@172.31.87.17:/var/lib/tomcat7/webapps/master.war'
    }
    stage('ContinuousTesting-test')
    {
        git 'https://github.com/selenium-saikrishna/FunctionalTesting.git'
    }
}

