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
                ansiblePlaybook installation: 'ansible', inventory: '/etc/ansible/hosts', playbook: '/etc/ansible/ansible-new/tom.yml', vaultTmpPath: ''
            }
        }
    }
}
