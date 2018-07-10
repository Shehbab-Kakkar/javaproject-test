pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh '/usr/share/ant/bin/ant done'
            }
        }
        stage('Test') {
            steps {
                sh 'java -jar bin/HelloWorld.jar'
            }
        }
        stage('Deploy') {
            steps {
                sh 'cp -v bin/HelloWorld.jar ~/'
            }
        }

         stage('Ansible') {
            steps {
                  //sh 'ansible-playbook -vv /etc/ansible/ansible.yaml -i /etc/ansible/hosts'
                  ansiblePlaybook become: true, colorized: true, disableHostKeyChecking: true, inventory: '/etc/ansible/hosts', playbook: '/etc/ansible/ansible.yaml'
            }
        }

    }
}
