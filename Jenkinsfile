node{
  
  stage('code build'){
    git 'https://github.com/yogeswari8/tomcat.git'
  }
  stage('build') {
    def mvnHome = tool name: 'maven3', type: 'maven'
    sh "${mvnHome}/mvn clean install"
  }
  stage('deploy to tomcat') {
    sh "chmod -f 777 /var/lib/jenkins/workspace/tomcat-webapp/target/travel.war"
    sh "cp -r /var/lib/jenkins/workspace/tomcat-webapp/target/travel.war /opt/apache-tomcat-9.0.56/webapps"
   }

}
