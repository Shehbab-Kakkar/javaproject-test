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
    }
}
