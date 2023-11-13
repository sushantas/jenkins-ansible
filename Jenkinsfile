pipeline{
agent any

 stages{

 stage('Checkout'){
  steps{
       git branch: 'main', credentialsId: 'git-credential', url: 'https://github.com/sushantas/jenkins-ansible.git'
       }
 }
 stage('AnsibleExecution'){
  steps{
     ansiblePlaybook credentialsId: 'auser', disableHostKeyChecking: true, installation: 'ansible', inventory: 'dhost.inv', playbook: 'apache.yml', vaultTmpPath: '' 
      }
    }
}
}
