pipeline{
  
  agent { label 'ansible' }

  stages{
      stage('checkout'){
            steps{
        git branch: 'PROD-TOMCAT-8080', url: 'https://github.com/saiteja6030/tomcat-ansible.git'
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


