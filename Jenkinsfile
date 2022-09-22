pipeline {
    environment {
    account          = "quickbooks2018"
    repo             = "jenkins-ansible-windows"
    
  }
    agent any
   
    stages {


    stage('SCM Checkout') {
    steps {

      git branch: 'main', url: 'https://github.com/quickbooks2018/jenkins-ansible-windows.git'
        
        }
         }


        stage('Ansible Playbooks in Gitlab Repo') {
            steps {
                sh '''
               
                ansible --version
                ansiblePlaybook credentialsId: 'windows2019', disableHostKeyChecking: true, installation: 'ansible', inventory: 'inventory', playbook: 'windowsplaybook.yaml'
                
                '''
             }
               
            }


        

        
    }
