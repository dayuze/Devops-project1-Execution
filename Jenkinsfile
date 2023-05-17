pipeline{
    agent any
    stages{
        stage('clone repo'){
            steps{
               git branch: 'main', url: 'https://github.com/Sonal0409/Devops-project1-Execution.git' 
            }
        }
        
        stage('Execute playbook'){
            
            steps{
                ansiblePlaybook credentialsId: 'hostid', disableHostKeyChecking: true, installation: 'myansible', inventory: 'dev.inv', playbook: 'dockerplaybook.yml'
            }
        }
    }
}
