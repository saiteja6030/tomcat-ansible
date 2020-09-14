pipeline{
  
  agent { label 'LIN-ANSIBEL-MASTER-172-31-33-11' }

  stages{
      stage('checkout'){
            steps{
        git branch: 'QA-TOMCAT-9090', url: 'https://github.com/svkvc1980/tomcat-ansible.git'
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
