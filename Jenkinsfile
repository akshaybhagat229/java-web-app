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
                         deploy adapters:[tomcat9(url:"",credentialsId:"")],war:'target/*.war'
                   }
           }
      }
}




  
