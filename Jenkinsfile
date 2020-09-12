peline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh 'echo "Executing ansible command"'
                //sh 'cd /home/centos/tomcat-8080/tomcat-ansible/'
		sh 'ansible -i hosts tomcat-setup.yml'
            }
        }
    }
}
