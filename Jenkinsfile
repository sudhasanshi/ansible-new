pipeline {
    agent any
    stages {
        stage('ansible') {
            steps {
			    sh 'rm -rf ansible-new'
                sh 'git clone https://github.com/sudhasanshi/ansible-new.git'
            }
        }
		stage('deploy') {
            steps {
                ansible-playbook '/etc/ansible/ansible-new/tomcat_download.yml'
            }
        }
    }
}
