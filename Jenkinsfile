pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh 'echo "Executing ansible command"'
                //sh 'cd /home/centos/tomcat-8080/tomcat-ansible/'
		sh 'ansible-playbook -i hosts tomcat-setup.yml'
            }
        }
    }
}
