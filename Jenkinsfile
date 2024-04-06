pipeline{
    agent any
    tools{
        maven 'maven3.9.6'
    }
    
    stages{
        stage('checkoutscmfrom git'){
            steps{
              git branch: 'main', credentialsId: 'ee357891-8f6c-4648-a4e7-cc4af280892d', url: 'https://github.com/Madhu04061989/springboot-hello.git'
            }
    
          }
        stage('Mavenbuild'){
            steps{
            sh "mvn clean install"
        }  
      }
    /*    
      stage('genertatereport'){
          steps{
          sh "mvn sonar:sonar"
          }
      }
      stage('copyartifacttonexus'){
          steps{
          sh "mvn clean deploy"
          }
      }
      stage('DeployappintoTomcat'){
          steps{
         sshagent(['18a8f4be-ac77-4288-bbf0-aa81851a646e']) {
             sh "scp -o StrictHostKeyChecking=no target/Amdproduction-1.0.war ec2-user@172.31.21.224:/opt/ApacheTomcat/webapps/"
           }
        }
      }
      */
    }   
}
