pipeline{
    agent any
        stages{
           stage('checkout code'){
                   steps{
                         git branch:'main',url:''
                   }
           }
        stage('build stage'){
                   steps{
                         sh '/opt/maven/bin/mvn clean package'
                   }
           }
        stage('Deployment'){
                   steps{
                         deploy adapters:[tomcat9(url:"http://54.152.175.108:8080/",credentialsId:"credential-tomcat")],war:'target/*.war'
                   }
           }
      }
}




  
