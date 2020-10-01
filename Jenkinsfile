pipeline {
    agent any
     
    stages {
      stage('checkout') {
           steps {
                git 'https://github.com/snteja/Simple-DevOps-Project.git'
          }
        }
        stage('Ansible') {
           steps {
                ansiblePlaybook become: true, credentialsId: 'ansible-ubuntu', disableHostKeyChecking: true, installation: 'myansible', inventory: 'hosts', playbook: 'tomcat.yml'
          }
        }
    }
}
