pipeline {
    agent any
    tools {
        ansible 'ansible' 
        }
   
    stages {


    stage('SCM Checkout') {
    steps {

      git branch: 'main', url: 'https://github.com/phongsakorn01/jenkins-ansible-windows.git'
        
        }
         }


        stage('Ansible Playbooks ') {
            steps {
             
                ansiblePlaybook credentialsId: 'windowserve',  installation: 'Ansible', inventory: 'inventory', playbook: 'windowsplaybook.yaml'
                
             }
               
            }


    }
        
    }
