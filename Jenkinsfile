node{
  
  stage('code build'){
    git 'https://github.com/yogeswari8/tomcat.git'
  }
  stage('build') {
    def mvnHome = tool name: 'maven3', type: 'maven'
    sh "${mvnHome}/mvn clean install"
  }
 

}
