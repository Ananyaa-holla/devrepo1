pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        git(url: 'https://github.com/Ananyaa-holla/devrepo1.git', branch: 'master', credentialsId: '3fea7c56-00c8-4549-8ba1-054a85e39342')
        sh '''sudo docker build -t ananyaahollab/jenkinsrepo:latest
sudo docker push ananyaahollab/jenkinsrepo:latest'''
      }
    }

    stage('Deploy') {
      steps {
        sh 'sudo docker run -d -p ananyaahollab/jenkinsrepo:latest'
      }
    }

  }
}