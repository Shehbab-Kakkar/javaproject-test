pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh '/usr/share/ant/bin/ant done'
      }
    }
  }
  stage('Deploy') {
      steps {
        sh 'cp -v /var/lib/jenkins/workspace/first-java-program/bin/HelloWorld.jar /root/Python'
      }
    }
}
