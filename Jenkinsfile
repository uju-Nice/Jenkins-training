
pipeline {
    agent any 

    stages{
        stage('Git Checkout'){
           steps{
            git credentialsId: '09820cf9-0047-4f02-93d4-a31e09ce5b38', url: 'https://github.com/uju-Nice/Jenkins-training/blob/master/Jenkinsfile'   
           } 
        }
        
        stage('Terraform init'){
           steps{
             sh 'terraform init'  
           } 
        }
        
         stage('Terraform apply'){
            steps{
               sh 'terraform apply --auto-approve' 
            }
         }
    }
}
