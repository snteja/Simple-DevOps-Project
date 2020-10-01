pipeline {
    agent any
     
    stages {
      stage('checkout') {
           steps {
             
                git branch: 'master', url: 'https://github.com/snteja/Simple-DevOps-Project.git'
          }
        }
        stage('Ansible') {
           steps {
                ansiblePlaybook become: true, credentialsId: 'ansible-ssh', disableHostKeyChecking: true, installation: 'myansible', inventory: 'hosts', playbook: 'tomcat.yml'
          }
        }
    }
}
