pipeline{
    tools{
        maven "mymaven"
    }
    agent any
    stages{
        stage("Clone the repo"){
            steps{
                git "https://github.com/rohitcheta/DECProject.git"
            }
        }
        stage("Execute playbook"){
            steps{
                ansiblePlaybook credentialsId: 'hostid', disableHostKeyChecking: true, installation: 'myansible', inventory: 'hostnames.inv', playbook: 'playbook.yml', vaultTmpPath: ''
            }
        }
    }
}
