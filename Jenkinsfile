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
                ansiblePlaybook become: true, disableHostKeyChecking: true, installation: 'myansible', inventory: 'hosts', playbook: 'tomcat.yml'
          }
        }
    }
}
