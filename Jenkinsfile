pipeline {
    environment {
    registry         = "registry.gitlab.com"   
    account          = "quickbooks2018"
    repo             = "gitlab-integration-with-jenkins"
    tag              = "latest"
    api_token_name   = "jenkins"
    gitlab_api_token = credentials('gitlab_api_token')
    
  }
    agent any
   
    stages {


    stage('SCM Checkout') {
    steps {

        git branch: 'main' , url: 'https://github.com/quickbooks2018/jenkins-ansible-windows.git'
        
        }
         }


        stage('Ansible Playbooks in Gitlab Repo') {
            steps {
                sh '''
               
                ansible --version
                
                '''
             }
               
            }


        

        
    }
}
