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
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}
