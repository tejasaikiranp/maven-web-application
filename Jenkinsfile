node
{
    def mavenHome = tool name: "maven3.8.4"
    
    stage('CheckoutCode')
    {
    git branch: 'development', credentialsId: '1bbb78b7-6e9e-4b1d-bd1d-83cfea50de77', url: 'https://github.com/tejasaikiranp/maven-web-application.git'
    }
    
    stage('Build'){
        sh "${mavenHome}/bin/mvn clean package"
    }
    /*
     stage('ExecuteSonarQubeReport'){
        sh "${mavenHome}/bin/mvn clean sonar:sonar"
     }
   
     stage('UploadArtifactIntoNexus'){
        sh "${mavenHome}/bin/mvn clean deploy"
    }
    
    stage('DeployAppintoTomcat'){
        sshagent(['07a5c535-2567-4910-9ec9-54a14c3b36b4']){
            sh "scp -o StrictHostKeyChecking=no target/maven-web-application.war ec2-user@13.235.81.135:/opt/apache-tomcat-10.0.21/webapps"
            
        }
    }
    */
    }
