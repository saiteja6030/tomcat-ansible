pipeline{
  
  agent { label 'Ansible' }

  stages{
      stage('checkout'){
            steps{
        git branch: 'QA-TOMCAT-9090', url: 'https://github.com/saiteja6030/tomcat-ansible.git'
    }
}
      stage('Build') {
            steps {
            sh 'echo "Executing ansible command"'
            sh 'ansible-playbook -i hosts tomcat-setup.yml'
            }
            }
  }

}


/* This is pretty basic
pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh 'echo "Executing ansible command"'
                //sh 'cd /home/centos/tomcat-8080/tomcat-ansible/'
		//sh 'ansible-playbook -i hosts tomcat-nodes tomcat-setup.yml'
		    sh 'ansible-playbook -i hosts tomcat-setup.yml -vvv' 
            }
        }
    }
}
*/
